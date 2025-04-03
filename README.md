# 🔍 Análise de Sentimentos com NLP

![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![NLP](https://img.shields.io/badge/NLP-TextBlob-orange)

Projeto para análise automática de sentimentos em textos, ideal para portfólio de Ciência de Dados.

## ⚙️ Como Usar
```python
from textblob import TextBlob

texto = "Adorei esse produto! Funciona perfeitamente."
analise = TextBlob(texto)
print(f"Sentimento: {'✅ Positivo' if analise.sentiment.polarity > 0 else '❌ Negativo'}")
```

#Resultados Esperados

Frase	Sentimento	Pontuação
"Ótimo atendimento!"	✅ Positivo	+0.8
"Não recomendo este serviço."	❌ Negativo	-0.6

#Aplicações Práticas
Análise de reviews na Amazon

Monitoramento de redes sociais

Chatbots com resposta emocional



3. Clique em **"Commit changes"**

---

#### **🐍 Passo 3: Adicionar o Código Python**
1. Clique em **"Add file" > "Create new file"**
2. No nome do arquivo, digite: `analise.py`
3. **Cole este código:**
```python
# Análise de Sentimentos Automática
from textblob import TextBlob

def analisar_sentimento(texto):
    analise = TextBlob(texto)
    polaridade = analise.sentiment.polarity
    if polaridade > 0:
        return "Positivo 😊", polaridade
    elif polaridade < 0:
        return "Negativo 😠", polaridade
    else:
        return "Neutro 😐", polaridade

# Teste
frases = [
    "Python é incrível para análise de dados!",
    "Odeio quando o código não funciona...",
    "Hoje está um dia normal."
]

for frase in frases:
    sentimento, score = analisar_sentimento(frase)
    print(f'"{frase}" -> {sentimento} (Score: {score:.2f})')
