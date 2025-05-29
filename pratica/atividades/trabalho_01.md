# Trabalho 01 - Projeto de um kit de desenvolvimento para microcontroladores STM32

## 1 - Objetivo

Este trabalho tem como objetivo apresentar uma visão geral da implementação do hardware de um sistema
embarcado. Tem como foco principal o projeto da fonte de alimentação, gestão do *clock*, controle do
*reset*, configuração do modo de *boot* e interface de gravação e *debug*.

Neste trabalho o estudante deverá realizar a especificação completa de todos os componentes eletrônicos,
elaborar o esquema elétrico e o **design** da placa de circuito impresso. Para realizar a captura do
esquemático e desenvolvimento da placa o estudante poderá utilizar o software que desejar. Entretanto,
devido a questões de custo, disponibilidade de documentação, suporte e exemplos, recomenda-se a utilização
do [KiCAD EDA](https://www.kicad.org/).

O estudante deverá incluir na entrega do trabalho os arquivos do projeto no formato original da ferramenta
CAD, tais como: esquemático, PCB (*Printed Circuit Board*), BOM (*Bill of Materials*), arquivos de
fabricação (*gerbers*), etc. Estes arquivos também deverão ser disponibilizados em formatos padrão, por
exemplo, **pdf**, **csv**, **xls**, entre outros. Além dos arquivos da ferramenta CAD, também deverá ser
elaborado um manual contendo uma descrição geral do kit, incluindo suas características e especificações,
mapa de pinos e intruções para utilização.

## 2 - Especificações

O kit desenvolvido deverá ser compatível com a especificação do **Arduino Nano**, disponível em 
[[1](https://docs.arduino.cc/hardware/nano/)]. Deverão ser observadas as dimensões e as funcionalidades de
cada pino. Caso existam divergências entre o mapa de pinos do **Arduino Nano** e do kit elas devem ser
devidamente apontadas no manual de utilização.

Assim como a plataforma **Arduino Nano**, o kit deverá possuir 3 diferentes possibilidades de alimentação,
são elas:

* **Conexão USB**: provavelmente esta será a forma mais comum de alimentar kit. A conexão USB não só
fornece energia, mas também possibilita a comunicação serial com um computador para programação e
monitoramento.

* **Pino Vin**: este pino pode ser utilizado para alimentar o kit através de baterias ou fontes externas de
maior tensão, deve suportar uma faixa de tensão de entrada de 7 a 12 volts. 

* **Pinos de 5V ou 3.3V**: estes pinos podem ser utilizados para alimentar diretamente o kit através de uma
fonte externa regulada.

Para oferecer maior flexibilidade no desenvolvimento de aplicações o kit deverá oferecer por padrão um
oscilador de cristal externo **HSE (High-Speed External Clock)** e um oscilador de cristal externo de baixa
velocidade **LSE (Low-Speed External Clock)** com uma frequência de 32.768 kHz.

Por padrão o kit deverá realizar o boot pela memória flash e, por meio de pressionamento de um botão, alterar
o boot para a memória do sistema. Opcionalmente a placa poderá incuir suporte ao boot pela memória RAM. Além
do botão para seleção de modo de boot deve ser incluído um botão de *reset*. O kit também deverá possuir um
LED e um botão de usuário e uma interface de gravação e *debug* **SWD (Serial Wire Debug)**.

## 3 - Referências

[1] [Arduino Nano](https://docs.arduino.cc/hardware/nano/)

[2] [KiCAD EDA](https://www.kicad.org/).

[3] [Getting started with STM32F4xxxx MCU hardware development](https://www.st.com/resource/en/application_note/an4488-getting-started-with-stm32f4xxxx-mcu-hardware-development-stmicroelectronics.pdf)