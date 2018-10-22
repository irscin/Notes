**Passo 1**
Para cada pixel do nosso plano de projeção, traçamos um raio do olho passando bem pelo meio do pixel. E
Então checamos cada objeto da cena para saber se o raio intersecta algume deles, caso haja mais de uma intersecção, ficamos com a intersecção do objeto mais próximo.
**Passo 2**
Traçamos o shadow ray, ou seja, o raio que vai do ponto de intersecção do raio primário com o objeto até a fonte de luz. Se há uma obstrução, então aquele ponto é sombreado, se o raio consegue chegar até a fonte de luz, então aquela área está iluminada.
**Passo 3**
Repetimos isso para cada pixel do plano bidimensional.
No fim, teremos uma representação em 2D da imagem 3D.
**Pseudocódigo**
```
for (int j = 0; j < imageHeight; ++j) { 
    for (int i = 0; i < imageWidth; ++i) { 
        // compute primary ray direction
        Ray primRay; 
        computePrimRay(i, j, &primRay); 
        // shoot prim ray in the scene and search for intersection
        Point pHit; 
        Normal nHit; 
        float minDist = INFINITY; 
        Object object = NULL; 
        for (int k = 0; k < objects.size(); ++k) { 
            if (Intersect(objects[k], primRay, &pHit, &nHit)) { 
                float distance = Distance(eyePosition, pHit); 
                if (distance < minDistance) { 
                    object = objects[k]; 
                    minDistance = distance; // update min distance 
                } 
            } 
        } 
        if (object != NULL) { 
            // compute illumination
            Ray shadowRay; 
            shadowRay.direction = lightPosition - pHit; 
            bool isShadow = false; 
            for (int k = 0; k < objects.size(); ++k) { 
                if (Intersect(objects[k], shadowRay)) { 
                    isInShadow = true; 
                    break; 
                } 
            } 
        } 
        if (!isInShadow) 
            pixels[i][j] = object->color * light.brightness; 
        else 
            pixels[i][j] = 0; 
    } 
} 
```
