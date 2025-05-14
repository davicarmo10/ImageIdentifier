# 🖼️ Classificador de Imagens com Scikit-learn

Este repositório contém um classificador de imagens desenvolvido em Python, utilizando técnicas de aprendizado de máquina com a biblioteca `scikit-learn`. O projeto tem como objetivo identificar imagens com base em características extraídas de seus dados.

---

## 📂 Estrutura do Notebook (`imageIdentifier.ipynb`)

### 1. **Importação de Bibliotecas**
O notebook utiliza as seguintes bibliotecas:

- `os`, `numpy`: manipulação de arquivos e arrays;
- `PIL (Pillow)`: carregamento e redimensionamento de imagens;
- `matplotlib`: visualização;
- `scikit-learn`: divisão de dados, padronização, redução de dimensionalidade (PCA) e classificação (SVM).

### 2. **Carregamento e Pré-processamento de Imagens**
As imagens são carregadas do diretório `imagens/`, convertidas para tons de cinza, redimensionadas para 50x50 pixels e achatadas em vetores unidimensionais:

```python
imagem = Image.open(caminho).convert('L')
imagem = imagem.resize((50, 50))
vetor = np.asarray(imagem).flatten()

3. Criação dos Vetores de Dados
dados: contém os vetores das imagens;

rotulos: contém os nomes das classes (cada subpasta representa uma classe).

4. Divisão dos Dados
Os dados são divididos em treino e teste utilizando:

train_test_split(dados, rotulos, test_size=0.2, random_state=42)

5. Padronização e Redução de Dimensionalidade
Padronização com StandardScaler

Redução de dimensionalidade com PCA para 100 componentes

6. Treinamento e Avaliação
Classificação com SVM (SVC)

Cálculo da acurácia

Geração da matriz de confusão

Exibição das imagens com suas respectivas classes previstas

📊 Resultados
O modelo exibe:

Acurácia de classificação

Matriz de confusão

Imagens de teste com o nome da classe prevista pelo modelo

🛠️ Como Usar
Coloque suas imagens organizadas em subpastas dentro de um diretório chamado imagens/.

Exemplo:

imagens/
  gato/
    img1.jpg
    img2.jpg
  cachorro/
    img1.jpg
    img2.jpg
Execute o notebook imageIdentifier.ipynb.

Verifique os resultados impressos e as imagens previstas.

📌 Requisitos
Instale as dependências com:

pip install numpy matplotlib pillow scikit-learn

📘 Observações
O classificador é sensível à qualidade e quantidade das imagens.

Resultados podem melhorar com o aumento da base de dados e ajuste de parâmetros.
