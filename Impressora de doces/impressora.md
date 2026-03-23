### Máquina Automatizada para Decoração de Doces

## Descrição do Projeto
O projeto consiste no desenvolvimento de um sistema mecatrônico para impressão direta de imagens e textos em superfícies de doces planos (como biscoitos, macarons e pães de mel) utilizando tinta comestível ou glacê. A arquitetura principal é composta por dois módulos integrados:

* **Módulo de alimentação:** Uma esteira rotativa (carrossel) acionada por motor de passo ou servomotor, para posicionar os doces.
* **Módulo de Impressão:** Um cabeçote de impressão a jato de tinta ou outro sistema de extrusão de fluidos viscosos para o glacê, acionado por motores ou um sistema pneumático, acoplado a um eixo que se desloca linearmente (e verticalmente?) sobre a superfície do doce. Ou um sistema estático onde a posição do doce é controlada pela esteira (talvez tenha menor custo mas maior complexidade).
* **Módulo de Controle:** Um controlador responsável por ler sensores de posição (encoders), acionar os motores e enviar os dados de imagem para o cabeçote no momento exato.

## MVP
O MVP do projeto é um protótipo consideravelmente simples: 

- **Mecânica:** Uma mesa rotativa em acrílico, alumínio ou PLA (ou material adequado para contato com alimentos) e uma estrutura para fixar o sistema de injeção, com mapeamento da posição e das coordenadas do cabeçote para impressão das figuras.
- **Controle:** Utilização de um microcontrolador (como ESP32 ou plataforma STM32) programado em C++ para gerenciar a cinemática do sistema.
- **Eletrônica:** Motor de passo (NEMA 17) para movimentar a esteira, garantindo torque e precisão, acionamento para o sistema de injeção com um sistema de extrusão pneumática ou por seringa motorizada.

## Tecnologias e Componentes

### Hardware & Mecânica
* **Estrutura:** Perfis de alumínio, chapas de acrílico/inox (foco em materiais *food-grade* ou de fácil higienização).
* **Atuadores:** Motores de passo (NEMA 17) para a mesa rotativa e cabrçote de deposição.
* **Eletrônica:** Microcontrolador (ESP32 / STM32), drivers de motor de passo (TMC2209/A4988), sensores de fim de curso e encoders rotativos.

### Software & Firmware
* **Linguagem Principal:** C++ estruturado para microcontroladores.
* **Controle:** Implementação de controladores digitais e malhas de controle (PID) para gerenciar a inércia da mesa rotativa, utilizando perfis de aceleração para evitar o deslizamento dos doces.
* **Modelagem:** Projetos mecânicos em CAD e mapeamento de coordenadas polares.

### Relevância
O setor de confeitaria tem uma demanda crescente por produtos personalizados (eventos corporativos, casamentos, datas comemorativas).
Uma solução automatizada de baixo/médio custo preenche a lacuna entre a produção puramente artesanal e as linhas de produção industriais de altíssimo custo, permitindo que pequenas e médias confeitarias ganhem escala, padronização e aumentem o valor agregado de seus produtos.

### Estimativa de Custo 
Os valores apresentados abaixo referem-se a uma estimativa para a construção do primeiro protótipo funcional (MVP) focado na deposição de fluidos viscosos (glacê ou chocolate). O orçamento prioriza a utilização de componentes de fabricação digital (impressão 3D e corte a laser) e eletrônica de prateleira (off-the-shelf) para manter o custo de validação baixo.

| Categoria | Componentes Principais | Custo Estimado (R$) |
| :--- | :--- | :--- |
| **Mecânica e Estrutura** | Perfis de alumínio estrutural, chapas de acrílico/PLA *food-grade*, rolamentos, fusos (para o eixo Z e seringa), correias e polias. | 450 - 850 |
| **Eletrônica e Atuadores** | Motores de passo NEMA 17 (Carrossel, Eixo Z e Extrusor), drivers (TMC2209/A4988), ESP32/STM32, fonte de alimentação, fins de curso e cabeamento. | 400 - 700 |
| **Sistema de Deposição** | Seringas de grau alimentício, peças complementares para a montagem da "bomba de seringa" acionada por motor ou atuador linear. | 150 - 350 |
| **Diversos e Consumíveis** | Elementos de fixação (parafusos, porcas), organizadores de cabos, consumíveis para testes (glacê, corantes). | 150 - 300 |
| **Total Estimado** | **Custo direto de materiais para o protótipo MVP** | **1.150 - 2.200** |
