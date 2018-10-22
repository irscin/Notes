- Apenas alguns poucos fótons chegam a atingir nossos olhos. Só podemos ver um ponto, se um fóton refletido ali chega a atingir nosso olho.
**==============FORWARD RAY TRACING==============**
- Forward Ray Tracing é uma técnica que "segue" o fóton da fonte de luz, passando pelo objeto o qual esse fóton atinge até chegar nos pixels do nosso canvas, ou seja, nossa superfície bidimensional de projeção.
- Há um problema com essa abordagem, entretanto, não tems como saber de antemão qual fóton irá atingir a superfície projetiva. Na verdade, uma porção minúscula desses fótons chega a atingir nosso olho. Sendo assim, renderizar imagens dessa forma causa um desperdício de poder computacional muito grande, visto que a maioria dessas trajetórias calculadas jamais serão usadas.
- Uma possível otimização seria "apontar" os fótons já na superfície de projeção e ver por qual pixel ele passa. Entretanto, essa abordagem não é genérica, visto que não pode prever como objetos difusos espalham a luz.
- Mesmo que fosse possível utilizar essa técnica, teríamos outro problema. Precisaríamos "pontilhar" o objeto com vários fótons até que este estivesse complemtamente "coberto" de fótons. O problema é que mesmo que aumentássemos a densidade de fótons, não podemos garantir que a superfície esteja toda coberta. Além do mais, calcular intersecções de raios de luz é uma tarefa muito cara computacionalmente, sendo assim, esta técnica seria muito custosa.
**==============BACKWARDS RAY TRACING==============**
- Como se pode imaginar, Backwards Ray Tracing simula objetos fazendo o caminho inverso da luz. Raios são disparados dos olhos até o objeto, então outro raio é disparado do objeto para a fonte luz, para se determinar se aquele ponto específico está sendo iluminado ou não.