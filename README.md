# 🎙️ Assistente de Voz Inteligente (Speech-to-Speech)

Um assistente virtual ponta a ponta construído no Google Colab. O sistema captura áudio do microfone via navegador, transcreve a fala usando OpenAI Whisper, processa a inteligência com o Google Gemini 2.5 Flash e sintetiza a resposta em voz utilizando gTTS.

Projeto prático de IA Generativa desenvolvido como parte do **Bootcamp Gen AI e Dados do Bradesco em parceria com a DIO**.

---

## 🚀 Como funciona o fluxo

O pipeline do projeto funciona em 4 etapas principais rodando inteiramente no navegador:

1. **Captura de Áudio (Microfone):** Utiliza uma ponte entre JavaScript e Python (`IPython.display`) para solicitar permissão e gravar o áudio do usuário diretamente no Google Colab.
2. **Transcrição (Speech-to-Text):** O áudio gravado em `.wav` é processado localmente pelo modelo **Whisper** (OpenAI), que transcreve a fala para texto com alta precisão.
3. **Processamento (LLM):** O texto transcrito é enviado via API para o **Google Gemini 2.5 Flash**, que atua como o "cérebro" do assistente, gerando uma resposta contextualizada.
4. **Síntese de Voz (Text-to-Speech):** A resposta em texto do Gemini é convertida novamente em áudio usando a biblioteca **gTTS** (Google Text-to-Speech) e reproduzida para o usuário.

---

## 🛠️ Tecnologias Utilizadas

* **Linguagens:** Python, JavaScript
* **Ambiente:** Google Colab
* **Modelos de IA:** * [OpenAI Whisper](https://github.com/openai/whisper) (Transcrição)
  * [Google Gemini API](https://ai.google.dev/) (Geração de Texto)
* **Bibliotecas auxiliares:** `gTTS` (Síntese de voz), `IPython` (Manipulação de mídia no notebook).

---

## ⚙️ Como executar o projeto

Como o projeto foi construído para o Google Colab, executá-lo é muito simples:

1. Faça um fork ou baixe o arquivo `.ipynb` deste repositório.
2. Faça o upload do arquivo no [Google Colab](https://colab.research.google.com/).
3. **Importante:** Você precisará de uma chave de API do Google Gemini. 
   * Acesse o [Google AI Studio](https://aistudio.google.com/) e gere a sua chave.
   * Cole a sua chave na variável correspondente no código: `client = genai.Client(api_key="SUA_CHAVE_AQUI")`.
4. Execute as células sequencialmente. O navegador pedirá permissão para acessar o seu microfone.
5. Fale a sua pergunta, aguarde o processamento e ouça a resposta!


---

## 👨‍💻 Autor

Desenvolvido por **Samuel** durante os estudos práticos de Inteligência Artificial Generativa.
