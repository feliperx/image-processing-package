# Projeto: Pacote de Processamento de Imagens

## Autora do Projeto: Karina Kato

#### Tecnologia: Python

#### Data: 23/10/2024

---

### Descrição

O pacote "image_processing-test" é usado para:

- Módulo "Processing":

  - Correspondência de histograma;
  - Similaridade estrutural;
  - Redimensionar imagem;

- Módulo "Utils":
  - Ler imagem;
  - Salvar imagem;
  - Plotar imagem;
  - Resultado do gráfico;
  - Plotar histograma;

---

## Passo a passo da configuração para hospedar um pacote em Python no ambiente de testes Test Pypi

- [x] Instalação das últimas versões de "setuptools" e "wheel"

```
py -m pip install --user --upgrade setuptools wheel
```

- [x] Tenha certeza que o diretório no terminal seja o mesmo do arquivo "setup.py"

```
py setup.py sdist bdist_wheel
```

- [x] Após completar a instalação, verifique se as pastas abaixo foram adicionadas ao projeto:

  - [x] build;
  - [x] dist;
  - [x] image_processing_test.egg-info.

- [x] Basta subir os arquivos, usando o Twine, para o Test Pypi:

```
py -m twine upload --repository testpypi dist/*
```

- [x] Após rodar o comando acima no terminal, será pedido para inserir o usuário e senha. Feito isso, o projeto estará hospedado no Test Pypi.hospedá-lo no Pypi diretamente.

## Instalação local, após hospedagem no Test Pypi

- [x] Instalação de dependências

```
pip install -r requirements.txt
```

- [x] Instalção do Pacote

Use o gerenciador de pacotes `pip install -i https://test.pypi.org/simple/ image-processing-test95`para instalar image_processing-test

```bash
pip install image-processing-test95
```

---

## Como usar em qualquer projeto

```python
from image-processing-test.processing import combination
combination.find_difference(image1, image2)
```

## Autor (quem hospedou o projeto no Test Pypi)

Felipe Xaud

## Licença

[MIT](https://choosealicense.com/licenses/mit/)
