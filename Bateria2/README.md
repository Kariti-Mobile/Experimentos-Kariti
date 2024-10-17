# Resultados de testes da segunda bateria

Nesta bateria, foram coletados dados de testes do Kariti na versão mobile em duas etapas.
  * Etapa 1: cadastro de usuário, de dados das provas e downloads dos cartões respostas gerados no aplicativo - etapa realizada pelo professor colaborador.
  * ETAPA 2: correção das provas usando o aplicativo - etapa realizada pelo professor colaborador.

Os dados dos experimentos estão organizados da seguinde forma:

O resultado de cada área estão contidos em suas respectivas pastas.

Para cada pasta/área contém;
* Uma pasta chamada **IMAGENS CARTOES** com as imagens dos cartões respostas submetidos a correção do Kariti (exceto na área de Engenharia Florestal - imagens perdidas devido a falhas técnicas).

* Uma planilha com **ANALISE DE TEMPO** das duas etapas de uso do aplicativo pelos professores no decorrer dos testes.

* Uma planilha contendo resultados da **ANALISE DE CORREÇÃO** do kariti mobile, composta por 8 colunas:
  
  * INFO 1: id das provas                            
  * INFO 2: id dos alunos                            
  * INFO 3: tipo de imagens - nesta bateria foram utilizadas imagens scanneadas em todos os casos                         
  * INFO 4: respostas marcadas nos cartões - leitura realizada pela equipe           
  * INFO 5: respostas lidas pelo Kariti para cada questão
  * INFO 6: comparativo de acertos do Kariti para cada questão
  * INFO 7: taxa de acerots do Kariti por prova
  * INFO 8: observações

 Os arquivos para análise e reprodução dos resultados de desempenho desta bateria podem ser obtidos nos links abaixo conforme a área:
  
  * [**Engenharia Florestal**](https://drive.google.com/drive/folders/14uIozrXHh0BCOEHawuRp_c6qrZ4pbu7Q?usp=drive_link)
  
  * [**Lincenciatura em Computação**](https://drive.google.com/drive/folders/1l5dHVSxe7SEiiKj484sp95ijBvIIBZ0A?usp=drive_link)
  
  * [**Geografia**](https://drive.google.com/drive/folders/1sBXvPwhwC2b2NImfYKWcWyDsT0q2mqxS?usp=drive_link)
  
  * [**Matemática**](https://drive.google.com/drive/folders/1sOm6uM0J-JmPTe4DNyII7n9HcAxEYRby?usp=drive_link)
  
  * [**Química**](https://drive.google.com/drive/folders/1_WGwChqmGMq-wP0reLwYYpi-h15OvB5F?usp=drive_link)

Para análise do questionários de usabilidade acesse: 

  * [**Análise Geral**](https://docs.google.com/spreadsheets/d/1mEh-yzPsXIu1RUQJ5Xb0T9VTLs5ajxbj/edit?usp=drive_link&ouid=109582750218571513653&rtpof=true&sd=true)
    
  * [**Questionários em PDF**](https://drive.google.com/file/d/18oFe8FsUObIQHJtASptPAx4uvexFBck2/view?usp=drive_link)

## Como reproduzir os testes ?

**Preparação de ambiente**: Para executar os códigos de correção de ambas as etapas, é necessário instalar previamente o Python 3.8.5 ou superior. Posteriormente, devem ser instalados os pacotes de dependência disponíveis em [aqui para download](../requirements.txt). Em posse do arquivo, execute `pip install -r requirements.txt` no terminal. Por fim, clone este repositório.

Abaixo será apresentada a forma de reprodução de um dos resultados referente a uma prova da área de Licenciatura em Computação, de modo que, com base nessa reprodução, os demais poderão também ser realizados alterando-se o nome da imagem do cartão de resposta (caminhos para todos os cartões de todas as áreas apresentados nos links acima).

1. Entre na pasta clonada e acesse a pasta Bateria2

   ```
   cd Experimentos-Kariti-2024\Bateria2
   ```
   
2. Execute o arquivo core.py passando o nome do arquivo da imagem do cartão de respostas como parâmetro. Aqui, usaremos o cartão do aluno de código 4 da prova 1 como exemplo. A imagem desse cartão pode ser observada abrindo o arquivo 1_4_7_5.png (na pasta atual) e os resultados desse cartão são apresentados na planilha acima citada. Para facilitar a compreensão, será apresentado abaixo um print dos resultados alcançados para serem posteriormente reproduzidos aqui.

   ![Resultados da primeira etapa para prova 1](https://github.com/user-attachments/assets/0e861a92-011c-414e-97cb-d0ad73ec66bf)


Nas primeiras colunas, são apresentadas as respostas do cartão de resposta digitados por humanos, como referência. Posteriormente, são apresentados os resultados obtivos pelo Kariti Core. Para visualizar esse comportamento, execute:

```
python core.py 1_4_7_5.png
```
Essa execução produzirá a saída abaixo, em que se observa na quinta informação separada por ponto-e-vírgula quais foram as respostas identificadas pelo Kariti Core (com A=1, B=2, C=3, D=4 e E=5). Assim, o Kariti Core identificou, nesta ordem, as seguintes respostas: A, A, A, C, A, A e A. Alcançando, portanto, 100% de taxa de acerto para essa prova.

![image](https://github.com/user-attachments/assets/39de578b-2a55-40a8-aa0f-506797f9c2a7)
