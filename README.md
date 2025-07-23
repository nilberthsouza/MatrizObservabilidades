# Matrizes de Observabilidade para Alocação de PMUs

Este repositório contém matrizes de observabilidade geradas para diferentes sistemas elétricos de potência, utilizadas no problema de alocação ótima de PMUs (Phasor Measurement Units).

## ⚙️ Formato dos Arquivos

Todos os arquivos estão no formato `.m` do MATLAB e podem ser carregados diretamente usando o comando `load()`.

### Sistemas Disponíveis:

Os seguintes sistemas estão disponíveis:

- `casoieee14P.m`
- `casoieee30P.m`
- `casoieee33P.m`
- `casoieee57P.m`
- `casoieee69P.m`
- `casoieee118P.m`
- `casoieee300P.m`
- `casoPeruvianP.m`
- `casoColombianp.m`

## 📌 Importante

As matrizes carregadas possuem uma **primeira coluna com zeros**, usada para controle interno.

Se for necessário obter a **matriz de observabilidade quadrada**, ou seja, apenas a parte correspondente à topologia do sistema, **exclua a primeira coluna** após o carregamento:

```matlab
MatObserv1 = load('casoieee14P.m');
MatObserv1 = MatObserv1(:, 2:end);  % Remove a primeira coluna
