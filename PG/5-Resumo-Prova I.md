- Iluminação global produz resultados mais realistas pois leva em consideração as interações entre os raios de luz e os objetos, as múltiplas reflexões e refrações, o "ricocheteamento" da luz entre vários objetos.
Algumas marcas do uso de iluminação global incluem:
- **Color Bleeding:** Um objeto que é colorido parcialmente pela reflexão vinda de outro objeto colorido
- **Soft Shadows:** As sombras passam de uma gradação suave da luz para a penumbra
- **Cáustica:** Padrões de luz especulares que são geradas pela reflexão/refração da luz em objetos difusos.
Objetos transparentes podem ser bastante esclarecedores em relação ao modelo de iluminação usado para renderizar a cena. Objetos transparentes renderizados com modelo de iluminação local são mais chapados e incapazes de produzir cáusticas.
- Radiância trata da luz em uma direção específica, já a irradiância trata da luz em todas as direções. Portanto, é mais adequado usar um sensor tratando-se de radiância.
- Mip Mapping é uma técnica usada para definir o nível de detalhes em texturas de objetos baseado nas distâncias entre os objetos e a câmera. Num objeto mais longe e, consequentemente, menor, uma textura de menor resolução pode ser usada pois não será notada a diferença.
- Filtragem anisotrópica consegue remover blur de imagens com mip maps e deixá-las mais nítidas.
- Ray Tracing não consegue produzir cáusticas pois estas ocorrem quando a luz se concentra num ponto, coisa que não ocorre no Ray Tracing, pois este apenas joga um raio por pixel.
- Path Tracing joga vários raios por pixel e cada raio segue apenas um caminho, não há "bifurcação" de raios como em Ray Tracing.