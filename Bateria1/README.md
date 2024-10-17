# **Resultados de testes da primeira bateria**

Nesta bateria, foram coletados resultados em duas etapas.

Após análise do resultado da primeira etapa, observou-se que o desempenho do Kariti estava abaixo do esperado. Com isso, foram realizadas alterações no módulo de correção e replicado os testes com a nova versão do Kariti - denominando-a de segunda etapa.

**OBS**. **NAS DUAS ETAPAS FORAM REALIZADOS OS TESTES UTILIZANDO OS MESMOS CARTÕES RESPOSTAS PREENCHIDOS (ENDEREÇO PARA DOWNLOAD DISPONÍVEL ABAIXO)**

Em cada etapa estão armazenados os resultados de 5 áreas separadas por pastas - listadas posteriormente.

Cada pasta/área contém uma pasta chamada **IMAGENS-CARTOES** com todas as imagens utilizadas nos teste da determinada área e uma planilha com os resultados de correção.

A planilha é composta por 8 informações:
  * INFO 1: id das provas                            
  * INFO 2: id dos alunos                            
  * INFO 3: tipo de imagens - nesta bateria foram utilizadas imagens scanneadas em todos os casos                         
  * INFO 4: respostas marcadas nos cartões - leitura realizada pela equipe com uma coluna para cada questão          
  * INFO 5: respostas lidas pelo Kariti - uma coluna para cada questão
  * INFO 6: comparativo de acertos do Kariti para cada questão
  * INFO 7: taxa de acerto do Kariti por prova
  * INFO 8: observações adicionais

**ETAPA 1**: planilha e imagens de cartões
  
  * [**Engenharia Florestal**](https://drive.google.com/drive/folders/1vdOpe2z-1R9QCWAHhGu8EjI3RYCK2dmR?usp=drive_link)
  
  * [**Lincenciatura em Computação**](https://drive.google.com/drive/folders/1-F5p1pxCkCyTHuRTXD9VwIbtSa_0Ky5F?usp=drive_link)
  
  * [**Geografia**](https://drive.google.com/drive/folders/1bvu3uqYXaX0jSVXLc5JLk6jr1nVc3Eq6?usp=drive_link)
  
  * [**Matemática**](https://drive.google.com/drive/folders/1AE9yZ8S4ivnZwtebqB8XWW9vyB7MgAR_?usp=drive_link)
  
  * [**Química**](https://drive.google.com/drive/folders/1yWxFRYng6wU8FaZAFhqjSMKgX9HjEOHw?usp=drive_link)
  
**ETAPA 2**: planilha e imagens de cartões
  
  * [**Engenharia Florestal**](https://drive.google.com/drive/folders/1HlIPCIyqhPNV08gmfWpft1ZJTD7WxJfI?usp=drive_link)
  
  * [**Lincenciatura em Computação**](https://drive.google.com/drive/folders/13CiVSJaUSDJ_BLm5c3SBLrB8QYnwxfNR?usp=drive_link)
  
  * [**Geografia**](https://drive.google.com/drive/folders/1kzteAFRs5qbjae_T7ffD7eNUIeZRvDyC?usp=drive_link)
  
  * [**Matemática**](https://drive.google.com/drive/folders/1Z7r7FItqive3M8ISNJvVBGjSBYQdt8Dd?usp=drive_link)
  
  * [**Química**](https://drive.google.com/drive/folders/1KeP2F39zn3ofKF1gLN_awl3TdXP27ORF?usp=drive_link)

# Como reproduzir os testes ?

**Preparação de ambiente**: Para executar os códigos de correção de ambas as etapas, é necessário instalar previamente o Python 3.8.5 ou superior. Posteriormente, devem ser instalados os pacotes de dependência disponíveis em [aqui para download](../requirements.txt). Em posse do arquivo, execute `pip install -r requirements.txt` no terminal. Por fim, clone este repositório.

**ETAPA 1**: Abaixo será apresentada a forma de reprodução de um dos resultados referente a uma prova da área de Química, de modo que, com base nessa reprodução, as demais poderão também ser realizados alterando-se o nome da imagem do cartão de resposta (caminhos para todos os cartões de todas as áreas apresentados nos links acima).

1. Entre na pasta clonada e acesse a pasta Bateria1

   ```
   cd Experimentos-Kariti-2024\Bateria1
   ```
   
2. Execute o arquivo core_etapa1.py passando o nome do arquivo da imagem do cartão de respostas como parâmetro. Aqui, usaremos o cartão do aluno de código 259 da prova 103 como exemplo. A imagem desse cartão pode ser observada abrindo o arquivo 103_259_10_5.png (na pasta atual) e os resultados desse cartão são apresentados na planilha acima citada. Para facilitar a compreensão, será apresentado abaixo um print dos resultados alcançados para serem posteriormente reproduzidos aqui.
   ![Resultados da primeira etapa para prova 259](https://github.com/user-attachments/assets/1a00cc92-29f4-448c-811a-a34147b984bc)

Nas primeiras colunas, são apresentadas as respostas do cartão de resposta digitados por humanos, como referência. Posteriormente, são apresentados os resultados obtivos pelo Kariti Core, que não conseguiu corrigir corretamente nenhuma das questões. Para visualizar esse comportamento, execute:

```
python core_etapa1.py 103_259_10_5.png
```
Essa execução produzirá a saída abaixo, em que se observa que o Kariti Core encontrou 11 marcadores de questões, porém, a prova possui apenas 10 questões. Logo, a prova não foi corrigida.

![image](https://github.com/user-attachments/assets/b1dca593-88fd-4eb4-b840-dbca0af2762d)


**ETAPA 2**: Abaixo será apresentada a forma de reprodução de resultados da mesma prova acima, contudo, podendo ser repetida para as demais provas alterando-se o nome da imagem do cartão de resposta (caminhos para todos os cartões de todas as áreas apresentados nos links acima).

1. Entre na pasta clonada e acesse a pasta Bateria1

   ```
   cd Experimentos-Kariti-2024\Bateria1
   ```
   
2. Execute o arquivo core_etapa2.py passando o nome do arquivo da imagem do cartão de respostas como parâmetro. Para facilitar a compreensão, será apresentado abaixo um print dos resultados alcançados (na segunda etapa) para serem posteriormente reproduzidos aqui.

![image](https://github.com/user-attachments/assets/e61f1060-8646-41c9-98e0-21427ccebad9)

Observa-se pela imagem que todas as questões foram corrigidas corretamente, como veremos na reprodução abaixo. Para isso, execute:

```
python core_etapa2.py 103_259_10_5.png
```

Essa execução produzirá a saída abaixo, em que se observa na quinta informação separada por ponto-e-vírgula quais foram as respostas identificadas pelo Kariti Core (com A=1, B=2, C=3, D=4 e E=5). Assim, o Kariti Core identificou, nesta ordem, as seguintes respostas: C, B, A, C, C, A, A, A, D e B. Alcançando, portanto, 100% de taxa de acerto para essa prova.

![image](https://github.com/user-attachments/assets/8195468d-5bfd-4de8-8c11-8943f35774e9)

  
