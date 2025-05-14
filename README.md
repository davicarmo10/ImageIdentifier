📘 Sobre o Projeto
Este repositório contém um classificador de imagens desenvolvido em Python, com foco em aprendizado de máquina supervisionado utilizando o scikit-learn. O projeto tem como objetivo identificar imagens com base em características extraídas de seus dados.

📂 Estrutura do Notebook
1. Importação de Bibliotecas
O notebook utiliza bibliotecas como:

os e numpy para manipulação de arquivos e arrays;

PIL para carregamento e redimensionamento de imagens;

matplotlib para visualização;

sklearn para divisão de dados, padronização, PCA e classificação com SVM.

2. Carregamento e Pré-processamento de Imagens
As imagens são lidas de um diretório imagens/, convertidas para tons de cinza, redimensionadas para 50x50 pixels e achatadas em vetores unidimensionais.

python
Copiar
Editar
imagem = Image.open(caminho).convert('L')
imagem = imagem.resize((50, 50))
vetor = np.asarray(imagem).flatten()
3. Criação dos Vetores de Dados
dados: contém os vetores das imagens;

rotulos: contém os nomes das classes (pastas com nomes diferentes representam classes distintas).

4. Divisão dos Dados
O conjunto é dividido em treino e teste com train_test_split.

5. Padronização e Redução de Dimensionalidade
Os dados são padronizados (StandardScaler) e reduzidos para 100 componentes principais com PCA.

6. Treinamento e Avaliação
Um classificador SVM (SVC) é treinado e testado. A acurácia e a matriz de confusão são apresentadas ao final.

📊 Resultados
O notebook imprime:

A acurácia do classificador.

A matriz de confusão.

Exibe algumas imagens de teste com a previsão feita pelo modelo.

🛠️ Como Usar
Coloque suas imagens organizadas em subpastas dentro de um diretório chamado imagens/. Cada subpasta deve representar uma classe (ex: gato/, cachorro/).

Execute o notebook imageIdentifier.ipynb.

Verifique os resultados impressos e visualizados.

📌 Requisitos
Instale as dependências com:

bash
Copiar
Editar
pip install numpy matplotlib pillow scikit-learn
