### Robô de Limpeza de Superfície Aquática (USV)

## Descrição do projeto

O projeto consiste no desenvolvimento de um robô autônomo capaz de realizar a coleta de resíduos na superfície de ambientes aquáticos de baixa turbulência, como lagoas, tanques e rios calmos.

Um exemplo de sistema similar é apresentado na Figura 01, onde observa-se uma estrutura com dois cascos (catamarã), um mecanismo de coleta baseado em esteira e uma unidade central de controle.

A embarcação funciona por meio de uma propulsão diferencial, onde o robô vai na direção dos resíduos que deseja coletar, permitindo que a esteira os coloque dentro de sua lixeira. Para isso, o robô necessita localizar onde o lixo se encontra, podendo utilizar sensores ou apenas uma rota pré-definida, onde foi visto que haveria resíduos no local, uma vez que a embarcação necessita ser assistida.

![USV.jpeg]
Figura 01 – Exemplo de robô de limpeza aquática.

Para o desenvolvimento do protótipo, será utilizada uma estrutura baseada em dois cascos de madeira compensada, garantindo flutuabilidade e estabilidade. O sistema contará com uma esteira motorizada responsável por coletar os resíduos e direcioná-los para um compartimento interno de armazenamento.

Para que o robô opere de forma autônoma, será necessário implementar um sistema de localização. No entanto, devido ao alto custo de módulos GPS de maior precisão, propõe-se o uso de técnicas alternativas, como triangulação baseada em sensores ou comunicação com pontos de referência. Além disso, será necessário desenvolver um método para identificação de regiões com presença de resíduos.

---

## MVP (Produto Mínimo Viável)

O desenvolvimento do projeto será dividido em três etapas evolutivas de MVP:

### **1º MVP – Protótipo básico em bancada**
- **Mecânica:** Construção inicial da estrutura em madeira compensada para testes estruturais
- **Controle:** Sistema embarcado capaz de acionar motores e realizar leitura básica de sensores
- **Eletrônica:** Desenvolvimento inicial do circuito (protoboard ou placa simples)

---

### **2º MVP – Sistema funcional controlado remotamente**
- **Mecânica:** Refinamento da estrutura
- **Controle:** Controle remoto do robô + inicio da programação dos sensores
- **Eletrônica:** Integração dos componentes e primeiras conexões embarcadas

---

### **3º MVP – Sistema semi-autônomo em ambiente real**
- **Mecânica:** Estrutura final funcional com propulsão e sistema de coleta operando na água
- **Controle:** Capacidade de navegação até resíduos e retorno a uma posição de referência
- **Eletrônica:** Sistema vedado, com alimentação estável e autonomia mínima de 1 hora, incluindo comunicação com a base e sensores ambientais

---

## Justificativa e relevância do problema abordado

Este projeto serve de auxílio na limpeza de lagos e rios, uma vez que permite que esses ambientes possuam a limpeza de suas superfícies sem que um ser humano necessite coletar os resíduos manualmente ou por meio de embarcações, sendo necessário apenas alguém para garantir que todo o processo seja realizado de maneira correta.

Como Joinville não apresenta muitos rios e lagos com presença constante de resíduos em suas superfícies, a cidade não possui uma forte necessidade do desenvolvimento do projeto. Porém, isso não pode ser generalizado para as demais cidades brasileiras, especialmente considerando que o Brasil não apresenta empresas com soluções consolidadas nessa área.

Em relação aos usuários, temos que seriam prefeituras ou órgãos ambientais, o que implica que seria mais difícil vender essa ideia, já que processos de licitação costumam ser demorados e dependem do interesse dos responsáveis em investir na preservação do meio ambiente.

--- 

## Estimativa de custos

- [Compensado naval](https://www.leroymerlin.com.br/compensado-de-virola-naval--160cm-x43cm-x-15mm-_1572464239?region=outros&gad_source=4&gad_campaignid=23037770349&gclid=Cj0KCQjwpv7NBhCzARIsADkIfWy5fv43boivnoikE_FycfBDJl8yRBF5TwMDRGYJKoBqiq5s6pXZ2EwaAvjnEALw_wcB) R$ 118

- [Hélices (brushless motor)](https://www.aliexpress.com/p/tesla-landing/index.html?src=google&src=google&albch=shopping&acnt=603-455-9033&slnk=&plac=&mtctp=&albbt=Google_7_shopping&gclsrc=aw.ds&albagn=888888&ds_e_adid=&ds_e_matchtype=&ds_e_device=c&ds_e_network=x&ds_e_product_group_id=&ds_e_product_id=pt1005007390065453&ds_e_product_merchant_id=5354444177&ds_e_product_country=BR&ds_e_product_language=pt&ds_e_product_channel=online&ds_e_product_store_id=&ds_url_v=2&albcp=23541406539&albag=&isSmbAutoCall=false&needSmbHouyi=false&gad_source=4&gad_campaignid=23551211716&gclid=Cj0KCQjwpv7NBhCzARIsADkIfWzrhlH6g11qIQgeLry7G4s-9RSYgH9QJ2F713VZASMveB-aIh7Izf4aAoqvEALw_wcB&aff_fcid=4e1e4d892b264d5f978f3288ca47315a-1774231076529-07227-irey5Th&aff_fsk=irey5Th&aff_platform=promotion&sk=irey5Th&aff_trace_key=4e1e4d892b264d5f978f3288ca47315a-1774231076529-07227-irey5Th&terminal_id=14ab908ba139424ca3b8ddcb167fb249&scenario=c_ppc_item_bridge&productId=1005007390065453&_immersiveMode=true&withMainCard=true&OLP=1128500808_f&o_s_id=1128500808&afSmartRedirect=n) R$ 120

- [ESC controller](https://www.aliexpress.com/p/tesla-landing/index.html?src=google&src=google&albch=shopping&acnt=603-455-9033&slnk=&plac=&mtctp=&albbt=Google_7_shopping&gclsrc=aw.ds&albagn=888888&ds_e_adid=&ds_e_matchtype=&ds_e_device=c&ds_e_network=x&ds_e_product_group_id=&ds_e_product_id=pt1005008353902037&ds_e_product_merchant_id=757826624&ds_e_product_country=BR&ds_e_product_language=pt&ds_e_product_channel=online&ds_e_product_store_id=&ds_url_v=2&albcp=23541406539&albag=&isSmbAutoCall=false&needSmbHouyi=false&gad_source=4&gad_campaignid=23551211716&gclid=Cj0KCQjwpv7NBhCzARIsADkIfWxWKPJUv2WEbbbzex2HlJ5KMdtxYNCOYR4DoO4z3icWxV47z2wyG_waAnJ4EALw_wcB&aff_fcid=dbbcf25419474292a443c6a0bc3aa90d-1774231025094-06978-irey5Th&aff_fsk=irey5Th&aff_platform=promotion&sk=irey5Th&aff_trace_key=dbbcf25419474292a443c6a0bc3aa90d-1774231025094-06978-irey5Th&terminal_id=14ab908ba139424ca3b8ddcb167fb249&scenario=c_ppc_item_bridge&productId=1005008353902037&_immersiveMode=true&withMainCard=true&OLP=1128500808_f&o_s_id=1128500808&afSmartRedirect=n) R$ 100

- [UWB - modulo de posicionamento](https://pt.aliexpress.com/item/1005001575673574.html?spm=a2g0o.tesla.0.0.2877zozizozijW&pdp_npi=6%40dis%21BRL%21R%242%2C33%21R%241%2C76%21%21%21%21%21%402101e62517742286940343513e8e6a%2112000044819351839%21btfpre%21%21%21%211%210%21&afTraceInfo=1005001575673574__pc__c_ppc_item_bridge_pc_main__yyPGtmA__1774228694102&gatewayAdapt=glo2bra) R$ 520
 
 ou

- [GPS BOM](https://pt.aliexpress.com/item/1005008148746092.html?spm=a2g0o.tesla.0.0.46f4oixPoixPFL&pdp_npi=6%40dis%21BRL%21R%241.515%2C76%21R%24621%2C46%21%21%21%21%21%40210319b717742312720161245e42c6%2112000043993857863%21btfpre%21%21%21%211%210%21&afTraceInfo=1005008148746092__pc__c_ppc_item_bridge_pc_main__8L5r8ak__1774231272097&gatewayAdapt=glo2bra) R$ 600

ou

- [Giroscópio](https://produto.mercadolivre.com.br/MLB-4531425137--modulo-de-sensor-gy-bno055-9dof-sensor-de-9-eixos-ahrs-_JM?matt_tool=72122373&matt_word=&matt_source=google&matt_campaign_id=23616672383&matt_ad_group_id=193482897349&matt_match_type=&matt_network=g&matt_device=c&matt_creative=798919494196&matt_keyword=&matt_ad_position=&matt_ad_type=pla&matt_merchant_id=5707786285&matt_product_id=MLB4531425137&matt_product_partition_id=2392713578861&matt_target_id=aud-1966919989813:pla-2392713578861&cq_src=google_ads&cq_cmp=23616672383&cq_net=g&cq_plt=gp&cq_med=pla&gad_source=1&gad_campaignid=23616672383&gclid=Cj0KCQjwpv7NBhCzARIsADkIfWyQzibCKBfDpBUFBoCqIFultnaymNNwgOeMicZm2x-xxm1lJwqNeUgaAnLCEALw_wcB) R$ 100

+

- [2 Comunicadores Lora](https://pt.aliexpress.com/item/1005006895440169.html?spm=a2g0o.tesla.0.0.278aJ6ptJ6ptpZ&pdp_npi=6%40dis%21BRL%21R%2468%2C70%21R%2435%2C99%21%21%21%21%21%402103274e17742318896196513eb1e6%2112000038666608542%21btfpre%21%21%21%211%210%21&afTraceInfo=1005006895440169__pc__c_ppc_item_bridge_pc_main__wWeaZwQ__1774231889702&gatewayAdapt=glo2bra) R$ 80

A ideia seria definir os limites em que o robô poderia operar e acompanhar sua trajetória por meio de uma base em terra, onde o operador utiliza o comunicador para alterar o funcionamento do robô, caso necessário.

- [ESP32](https://www.mercadolivre.com.br/esp32-30-pino-doit-devkit-com-esp32wroom32-wifi-bluetooth/up/MLBU2845641474?pdp_filters=item_id%3AMLB3914402941&from=gshop&matt_tool=97904134&matt_internal_campaign_id=340493280&matt_word=&matt_source=google&matt_campaign_id=22883155151&matt_ad_group_id=189401224961&matt_match_type=&matt_network=g&matt_device=c&matt_creative=775468301405&matt_keyword=&matt_ad_position=&matt_ad_type=pla&matt_merchant_id=5336131774&matt_product_id=MLBU2845641474&matt_product_partition_id=2443836665998&matt_target_id=aud-1966919989813:pla-2443836665998&cq_src=google_ads&cq_cmp=22883155151&cq_net=g&cq_plt=gp&cq_med=pla&gad_source=1&gad_campaignid=22883155151&gclid=Cj0KCQjwpv7NBhCzARIsADkIfWxCevrHvBIvz44eKoKig_r1LI0WWRpkgrVWnbvgMvLLmBnDkGuBG_IaAgF8EALw_wcB) R$ 40


 - [Bateria 3S](https://www.mercadolivre.com.br/kit-2-baterias-turnigy-2200mah-3s-25c-drones-aero-auto-heli/up/MLBU1455229086?pdp_filters=item_id%3AMLB3857838479&from=gshop&matt_tool=31240533&matt_word=&matt_source=google&matt_campaign_id=23351282051&matt_ad_group_id=195616641248&matt_match_type=&matt_network=g&matt_device=c&matt_creative=787871585033&matt_keyword=&matt_ad_position=&matt_ad_type=pla&matt_merchant_id=5711878231&matt_product_id=MLBU1455229086&matt_product_partition_id=2389272460553&matt_target_id=aud-1966919989813:pla-2389272460553&cq_src=google_ads&cq_cmp=23351282051&cq_net=g&cq_plt=gp&cq_med=pla&gad_source=1&gad_campaignid=23351282051&gclid=Cj0KCQjwpv7NBhCzARIsADkIfWxN3uqfORW4vzM_wsStCTZ1vBalFoz540EibpDsF02MySXJuoBbPWcaAjZGEALw_wcB) R$ 500

Não foi incluída no orçamento a parte da esteira com motor, pois ela não é necessariamente essencial para o protótipo inicial, uma vez que o robô pode atuar apenas como uma estrutura coletora, onde o lixo fica retido devido à direção do movimento.

Além disso, alguns custos intermediários, como jumpers, placas, conectores e materiais de vedação, não foram considerados.

Por fim, o custo estimado é de R$ 1058 ao considerar a solução com giroscópio + LoRa. Considerando os custos adicionais não listados, pode-se estimar que o projeto fique na faixa de: **R$ 1500 a R$ 1900**.


---

## Possíveis desafios técnicos

Entre os principais desafios, temos:

- **Alimentação:** A alimentação do sistema deve suportar a comunicação por rádio/Wi-Fi, os motores, talvez uma câmera e os demais sensores, além de necessitar de um isolamento muito bem projetado para garantir que não entre água no sistema.

- **Reconhecimento do lixo:** Existem 2 formas de projetar: uma em que o robô possui uma rota definida por alguém em terra e a executa; e outra em que o robô possui algum mecanismo para identificar os dejetos, como uma câmera com IA ou outro tipo de sensoriamento.

- **Posicionamento:** O uso de um GPS decente iria encarecer o projeto de maneira astronômica, e um módulo UWB custa em torno de R$ 130, portanto uma triangulação também não é muito viável em relação ao custo. Portanto, deve-se pensar em como reduzir esses custos. Outra solução pensada seria utilizar um giroscópio BNO055 e definir quanto que o robô deve andar em cada direção, onde pode-se adicionar um GPS vagabundo para corrigir o erro do giroscópio. Esta solução é suficiente em um caso de uma lagoa em que a água é praticamente parada.
---

## Estratégia de desenvolvimento

O projeto necessitará de, aproximadamente, 2 pessoas focadas na eletrônica e no desenvolvimento do código. No entanto, o desenvolvimento da estrutura mecânica também não será simples para apenas uma pessoa, sendo interessante que haja alguém com conhecimento tanto em mecânica quanto em programação, para garantir a integração entre as áreas.

A equipe de eletrônica será responsável por montar um protótipo inicial com dois motores e os sensores escolhidos, permitindo que a equipe de software inicie o desenvolvimento do controle do sistema. Paralelamente, a equipe de mecânica irá focar na construção da estrutura do catamarã e, posteriormente, na integração da parte central do robô.

O ideal é que a equipe de software consiga focar o quanto antes na forma como os resíduos serão coletados e como o robô irá se orientar, pois creio que esta será a parte mais difícil.

Para realizar a integração, a equipe de eletrônica e a de mecânica deverão estar prontas, de modo que seja possível instalar toda a eletrônica no robô e garantir sua vedação. Em seguida, será interessante realizar testes em uma piscina (disponível para o grupo), para verificar se tudo está conforme o esperado. Enquanto isso, o software pode realizar testes de forma independente, sem estar conectado à planta.

Na integração final, será interessante realizar testes em um ambiente real, provavelmente uma lagoa aberta, podendo ser adicionados alguns dejetos para verificar se o robô irá funcionar corretamente. Em relação a isso, acredito que seja possível providenciar um local adequado para a realização desses testes.