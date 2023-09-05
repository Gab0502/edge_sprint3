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
  </ul>
</nav>
<p>Tambem será necessario seguir draft do projeto para seu funcionamento</p>
<figure>
  <img src="https://github.com/Gab0502/edge_sprint3/assets/104799843/5914f449-3fc2-45ef-a620-58a118cd8528">
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
