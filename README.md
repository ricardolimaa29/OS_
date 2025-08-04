# Aula Prática: Módulo `os` no Python

---

## Parte 1: Introdução

**O que é o módulo **``**?**

- É um módulo interno do Python que permite interagir com o sistema operacional (Windows, Linux ou Mac).
- Pode ser usado para criar pastas, listar arquivos, apagar, renomear e muito mais.

**Importação:**

```python
import os
```

---

## Parte 2: Exemplos Práticos

### 1. Mostrar onde o script está rodando

```python
import os
print("Diretório atual:")
print(os.getcwd())
```

**Objetivo:** Entender onde os arquivos estão sendo criados ou lidos.

---

### 2. Criar e remover pastas

```python
os.mkdir("NovaPasta")
print("Pasta criada!")

os.rmdir("NovaPasta")
print("Pasta removida!")
```
*
open("Projetos/matematica.txt", "w").close()
open("Projetos/portugues.txt", "w").close()
open("Projetos/ciencias.txt", "w").close()
*

**Objetivo:** Mostrar como criar organização de pastas por código.

---

### 3. Listar arquivos da pasta atual

```python
arquivos = os.listdir()
for item in arquivos:
    print(item)
```

**Objetivo:** Ver na tela o que existe na pasta.

---

### 4. Criar arquivos automaticamente

```python
for i in range(1, 4):
    nome = f"relatorio_{i}.txt"
    with open(nome, "w") as arq:
        arq.write("Conteúdo gerado por Python\n")
    print(f"{nome} criado")
```

**Objetivo:** Mostrar como criar arquivos em lote.

---

### 5. Renomear um arquivo

```python
os.rename("relatorio_1.txt", "relatorio_final.txt")
```

**Objetivo:** Demonstrar como corrigir ou organizar nomes de arquivos.

---

### 6. Apagar arquivos (com verificação de existência)

```python
if os.path.exists("relatorio_final.txt"):
    os.remove("relatorio_final.txt")
    print("Arquivo apagado")
else:
    print("Arquivo não encontrado")
```

**Objetivo:** Ensinar cuidado e responsabilidade digital.

---

### 7. Saber qual sistema operacional está rodando

```python
print("Sistema operacional:", os.name)
```

**Objetivo:** Mostrar que códigos podem se adaptar ao sistema do usuário.

---

## Atividade Final (em dupla ou trio)

**Desafio:** Criar um script que:

1. Crie uma pasta chamada `Projetos`
2. Dentro dela, crie arquivos `matematica.txt`, `portugues.txt`, `ciencias.txt`
3. Liste os arquivos criados na tela
4. Renomeie um deles para `historia.txt`
5. Remova um deles (com verificação)

**Objetivo:** Consolidar os conceitos com algo prático e real.

---

