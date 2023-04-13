## Instalar o conda
1. Baixar o arquivo em: https://www.anaconda.com/products/distribution
2. Rodar no terminal:
```bash
$ bash Anaconda-latest-Linux-x86_64.sh
```

## Gerenciar ambientes conda
Tutorial: https://conda.io/projects/conda/en/latest/user-guide/tasks/manage-environments.html

## Criar ambiente através de arquivo yaml
1. Criar o yaml como no exemplo
```yaml
name: data-science
channels:
  - conda-forge
  - defaults
dependencies:
  - python==3.10
  - pip
  - pandas==2.0.0
  - scikit-learn
  - jupyterlab
  - matplotlib
  - pip:
    - networkx
```
O ideal é que você informe a versão de todas as bibliotecas que vai instalar.

2. Rodar no terminal
```bash
$ conda env create -n data-science --file data-science.yaml
```
3. Ative o ambiente com
```bash
$ conda activate data-science
```
No terminal vai aparecer algo como `(data-science) $`.

4. Abrir o jupyter lab de dentro do ambiente
```
(data-science) $ jupyter lab
```

Obs: cada ambiente diferente deve ter o jupyter lab instalado para que você consiga usá-lo, mas há um truque pra evitar ter que ficar trocando de ambiente: é possível instalar um ambiente já criado como um kernel do jupyter.

## Instalar um env do conda como kernel
1. Ative o ambiente desejado
2. Rode no terminal
```bash
$ ipython kernel install --user --name=my-env
```
3. De qualquer ambiente que tenha o jupyter lab instalado o ambiente vai aparecer como uma das opções para rodar seu código.

4. Se quiser desinstalar um kernel rode
```bash
$ jupyter kernelspec uninstall new-env
```

## Criar um environment.yml a partir de um conda env
1. Ative o ambiente e rode
```bash
<meu_env>:$ conda env export >> environment.yml
```

Obs: ver a lista de pacotes em um ambiente
```bash
$ conda list -n myenv
```