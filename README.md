# Bloquear Digitação Manual em Input (Somente Leitor de Código de Barras)

Este projeto demonstra como bloquear completamente a digitação manual em um campo `<input>` HTML, permitindo somente a entrada via **leitor de código de barras**.  
O script detecta a velocidade de digitação e impede qualquer tentativa de digitação humana ou colagem.

## 🚀 Funcionalidade

- Bloqueia **digitação manual** (teclado).
- Bloqueia **colagem** (Ctrl+V).
- Aceita apenas entrada via **leitores de código de barras**.
- Detecta automaticamente quando o código termina.
- Compatível com navegadores antigos (IE8+).

## 🧠 Como funciona

- Se o intervalo entre teclas for maior que **70 ms**, o texto é descartado (característica de digitação manual).
- Teclas especiais (Enter, Shift, Tab etc.) são ignoradas.
- A função `preventDefault()` impede qualquer caractere digitado manualmente.
- O evento `paste` é bloqueado.
- A função `processBarcode()` recebe o código final lido.

## 📂 Estrutura

```
index.html
│
└── HTML + JavaScript para bloquear digitação humana
```

## 🖥 Exemplo de Uso

Abra o arquivo `index.html` no navegador e escaneie um código de barras.  
O input:

- Não aceita teclas digitadas manualmente  
- Não permite colagem  
- Só exibe valores vindos do scanner  
