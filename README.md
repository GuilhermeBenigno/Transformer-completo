# Transformer From Scratch - Lab 4

##  Descrição

Este projeto implementa um Transformer completo (Encoder + Decoder) utilizando apenas NumPy, baseado no paper "Attention Is All You Need".

O objetivo é demonstrar o funcionamento interno da arquitetura Transformer sem uso de frameworks de alto nível.

---

##  Arquitetura

O modelo é composto por:

###  Encoder
- Self-Attention
- Add & Norm
- Feed Forward Network (FFN)

###  Decoder
- Masked Self-Attention
- Cross-Attention (usa saída do Encoder)
- Add & Norm
- FFN
- Camada Linear + Softmax

---

##  Fluxo de Execução

1. A entrada é convertida em embeddings
2. O Encoder gera uma representação contextual (encoder_output)
3. O Decoder gera a saída token por token:
   - Aplica máscara causal
   - Usa cross-attention com o encoder
4. O processo continua até gerar `<EOS>`

---

##  Como Executar

```bash
pip install numpy
python transformer_complete.py

## 🤖 Uso de IA

Partes do código foram geradas/complementadas com auxílio de IA, sendo totalmente revisadas, compreendidas e adaptadas pelo aluno.
