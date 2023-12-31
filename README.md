<h1>Sistema de Monitoramento de Esgotos- grupo DESKTOPS</h1>
<h2>Descrição</h2>
<p>
Nosso projeto consiste em um website e aplicativo que tentará resolver  a problemática situação das enchentes em São Paulo. Utilizando sensores estrategicamente posicionados nos sistemas de esgoto da cidade, nosso objetivo é fornecer alertas antecipados à população e às autoridades sobre possíveis enchentes em vias públicas do estado. Estes sensores enviarão dados em tempo real para o site, permitindo que as pessoas se preparem adequadamente e, assim, minimizem ou até mesmo previnam os danos decorrentes desse desastre natural.
</p>
<figure>
  <img src="https://github.com/Gab0502/edge_sprint3/assets/104799843/df1e726d-8135-4853-bd1d-e83d667061fa">

  
  <figurecaption>arquitetura do projeto</figurecaption>
</figure>

<hr>

<h2>Componentes Hardware</h2>
<p>Para montar um sensor do projeto será utilizados os seguintes componentes:</p>
<nav>
  <ul>
    <li>1x Placa wireless - ESP32</li>
    <li>1x Sensor de distancia ultrassonico - HC-SR04</li>
    <li>1x Modulo sensor velocidade/encoder</li>
    <li>1x sensor de profundidade - FD10</li>
    <li>1x servo motor - MG90D</li>
  </ul>
</nav>
<p>Tambem será necessario seguir draft do projeto para seu funcionamento</p>
<figure>
  <img src="https://github.com/Gab0502/edge_sprint3/assets/104799843/3f0ec246-d85b-4e4e-b81e-60fd4d5fadbb">
  <br>
  <figurecaption>Visão geral</figurecaption>
</figure>

<hr>
<h2>Funcionamento</h2>
<p>O sistema contará com dois sensores que trabalharão em conjunto que funcionarão da seguinte forma: </p>

<h3>Sensor de RPM:</h3>

<figure>
  <img src="https://github.com/Gab0502/edge_sprint3/assets/104799843/7c10db10-bc08-45c7-89f2-857d5c24936c">
  <br>
</figure>
<p>O sensor em questão será posicionado ao nível padrão da água no local. Ele consiste em um módulo de sensor de velocidade/encoder, bem como duas rodas: uma roda (1) com vários furos em sua parte interna e outra roda (2) com pequenas nadadeiras em seu contorno. A primeira roda será acomodada dentro de uma caixa lacrada, posicionada no centro dos sensores. A segunda roda será colocada fora da caixa e conectada à primeira por meio de uma pequena haste.

Quando o fluxo de água faz a roda externa (2) girar, seguindo a lei da velocidade angular, esse movimento é replicado pela roda interna (1) localizada dentro da caixa. Essa configuração permite o funcionamento do sensor de rotações por minuto (RPM). O movimento da roda dentro da caixa resulta na obstrução repetida e desobstrução do sensor infravermelho presente no dispositivo. Esse sensor ativa uma função que registra quantas vezes isso ocorre a cada segundo e, em seguida, realiza os cálculos necessários para determinar a velocidade do fluxo de água em RPM.</p>

<h3>Sensor de nivel de água:</h3>

<figure>
  <img src="https://github.com/Gab0502/edge_sprint3/assets/104799843/4b0e6d3d-03e6-4e20-80e3-038d86b4fe42">
  <br>
  <figurecaption>Visão Frontal</figurecaption>
</figure>
<br>
<figure>
  <img src="https://github.com/Gab0502/edge_sprint3/assets/104799843/359dfcc7-4231-478b-b9ea-1b69758fd8cf">
  <br>
  <figurecaption>Visão Lateral</figurecaption>
</figure>
<br>
<figure>
  <img src="https://github.com/Gab0502/edge_sprint3/assets/104799843/084320a0-9382-4d3a-9a19-b3fc5b402a77">
  <br>
  <figurecaption>Visão Inferior</figurecaption>
</figure>
<br>
<figure>
  <img src="https://github.com/Gab0502/edge_sprint3/assets/104799843/c45569b3-bbfa-45e7-bdaf-72920b2e5c83">
  <br>
  <figurecaption>sistema de proteção desativado</figurecaption>
</figure>
<br>
<figure>
  <img src="https://github.com/Gab0502/edge_sprint3/assets/104799843/f113bcb4-7dc0-4ada-b2f0-48780abd1f53">
  <br>
  <figurecaption>sistema de proteção ativado</figurecaption>
</figure>
<br>
<p>
O sensor de nível de água é um dispositivo de funcionamento simples. Ele consiste em um sensor ultrassônico (1.) posicionado dentro de uma caixa com pequenos orifícios, permitindo que o som seja emitido e retornado para medir a distância entre o sensor e a água. Esta caixa também abriga o ESP32 (4.), localizado em um compartimento separado para maior proteção em caso de enchentes.

Para evitar que a água entre em contato com o sistema, implementamos uma função de proteção. O sensor ultrassônico inicialmente faz leituras. Se a água atingir uma altura específica, que pode variar de acordo com o tamanho do esgoto, o sistema ativa a função de proteção. Um servo motor entra em ação, empurrando uma placa de material leve e sólido, como acrílico, para cobrir os pequenos orifícios. Essa placa também possui uma camada de borracha ao redor para proporcionar uma barreira adicional contra a entrada de água.

O sistema permanece em modo de proteção com sua entrada bloqueada por 5 minutos. Após esse período, o sensor de profundidade de água (2.) verifica se a caixa ainda está submersa. Se detectar que a caixa está embaixo d'água, o sistema continua em modo de proteção até que não haja mais detecção de submersão. Se a detecção inicial de altura for causada apenas por um objeto grande que tenha passado pelo esgoto, após os primeiros 5 minutos de verificação para garantir a integridade do sistema, o sensor não detectará mais água e retornará ao funcionamento normal."
</p>

<h2>Integrantes</h2>
<p>Caíque Walter Silva - RM 550693</p>
<p>Enrico Enricco Rossi - RM 551717</p>
<p>Gabriel Marquez Trevisan - RM 99227</p>
<p>Guilherme Nobre Bernardo - RM 908604</p>
<p>Silvia Kavabata - RM 97650</p>





