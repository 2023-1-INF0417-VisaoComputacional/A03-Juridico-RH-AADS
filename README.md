# People tracking utilizando uma câmera acoplada no gimbal e suas aplicações

## Resumo

O rastreamento de pessoas é uma tarefa essencial na área de visão computacional e robótica, com aplicações práticas em segurança, vigilância e navegação autônoma. Neste artigo, apresentamos uma proposta de solução que combina técnicas de aprendizado profundo, detecção de objetos e rastreamento por correspondência para alcançar um rastreamento robusto. Além disso, integramos o sistema em uma câmera equipada com um gimbal, permitindo o acompanhamento do alvo. A proposta visa superar desafios como variações de iluminação, fundos complexos e presença de múltiplas pessoas. Além disso, é suposto que o artigo traga aplicações da tarefa proposta e comente sobre os resultados obtidos.

## Palavras Chave: 
Tracking, YOLO, Visão computacional, Gimbal

## Introdução

O rastreamento robusto de pessoas tem sido objeto de interesse crescente devido à sua importância em diversas aplicações práticas. Este artigo propõe uma abordagem baseada em inteligência artificial (IA), que utiliza técnicas de aprendizado profundo para detecção de objetos e rastreamento por correspondência para acompanhar com precisão a trajetória de pessoas em sequências de vídeo ou em tempo real. Além disso, a integração com um gimbal possibilita o movimento automático da câmera, mantendo o alvo centralizado no quadro, ampliando ainda mais a utilidade do sistema.

O problema de rastreamento robusto de pessoas abrange diversas áreas de aplicação, como segurança e vigilância [1], análise de multidões, navegação autônoma, interatividade em jogos e realidade aumentada, e monitoramento de saúde e esportes[2]. Em cenários de segurança, o rastreamento auxilia na detecção de comportamentos suspeitos e monitoramento de espaços públicos. Já na análise de multidões, é utilizado para entender o fluxo de pessoas em eventos ou locais movimentados. Em veículos autônomos ou drones, o rastreamento permite seguir alvos em movimento e evitar colisões. Nos campos de jogos e realidade aumentada, é fundamental para a interação com elementos virtuais no mundo real, e em aplicações de monitoramento de saúde ou esportes, possibilita a análise de postura e movimentos específicos.


## Fundamentação teórica

Nossa proposta de solução baseia-se em uma combinação de técnicas de aprendizado profundo, detecção de objetos e rastreamento por correspondência. Inicialmente, utilizamos algoritmos de detecção de objetos, como YOLO (You Only Look Once) [3] ou Faster R-CNN, para identificar e delimitar as pessoas em cada frame do vídeo. Em seguida, aplicamos métodos de rastreamento por correspondência, considerando informações de posição, tamanho e características dos objetos para estabelecer correspondências entre frames consecutivos.

Uma forma utilizada de melhorar a robustez e suavidade do rastreamento, é empregar técnicas de filtragem de dados, como o Filtro de Kalman ou o Filtro de Partículas. Esses métodos reduzem ruídos e incertezas, resultando em um rastreamento mais preciso e confiável.

Para viabilizar o rastreamento de objetos no âmbito do hardware, foi utilizado um gimbal, que é um dispositivo mecânico que permite o movimento controlado da câmera em duas ou três direções, geralmente pan (movimento horizontal), tilt (movimento vertical) e roll (rotação). Além disso, é fundamental para person tracking implementar um controle de posicionamento que receba as informações de rastreamento do objeto e movimente o gimbal de forma a manter a pessoa rastreada centralizada no quadro. Essa centralização pode ser feita de algumas maneiras, uma possível seria a extração do centróide da Bounding box da pessoa e centralizar esse ponto no quadro da câmera.

Uma das abordagens mais promissoras para a tarefa de rastreamento robusto de pessoas é a utilização do YOLOv8, um modelo de última geração que se baseia no sucesso das versões anteriores do YOLO (You Only Look Once). O YOLOv8 apresenta novos recursos e melhorias significativas, visando aumentar ainda mais o desempenho e a flexibilidade do modelo.

O YOLOv8 foi projetado com foco em três principais atributos: velocidade, precisão e facilidade de uso. Essa combinação torna-o uma excelente escolha para uma ampla gama de tarefas, incluindo detecção e rastreamento de objetos, segmentação de instâncias, classificação de imagens e estimativa de pose.

A integração da câmera com os servos do gimbal oferece uma solução robusta e versátil para o problema de person tracking, possibilitando a captura de dados precisos em tempo real e abrindo caminho para aplicações em áreas como segurança, monitoramento e interação humano-máquina. Ao longo deste artigo, serão abordadas as metodologias utilizadas para processamento das informações provenientes dessas tecnologias, bem como sua aplicação prática na tarefa de rastreamento personalizado.

## Referências

[1] ROOKSBY, John et al. Personal tracking as lived informatics. In: Proceedings of the SIGCHI conference on human factors in computing systems. 2014. p. 1163-1172.


[2] FUNG, Ng Ming et al. Elderly fall detection and location tracking system using heterogeneous wireless networks. In: 2019 IEEE 9th Symposium on Computer Applications & Industrial Electronics (ISCAIE). IEEE, 2019. p. 44-49.


[3]ULTRALYTICS. Documentação Oficial. Disponível em: https://docs.ultralytics.com/. Acesso em: 03 ago. 2023, às 22:15.
