# Qual-esse-rem-dio-
# REMEDIO

Aplicativo Android (POC) feito em Kotlin com Jetpack Compose para identificar o nome de um medicamento a partir de uma foto usando OCR do **Google ML Kit (Text Recognition on device)**. O fluxo do app é simples: o usuário captura a imagem, recorta a área relevante para melhorar o reconhecimento, o texto é extraído localmente no aparelho e o app tenta limpar e selecionar o melhor termo para pesquisa. Caso o OCR não reconheça perfeitamente, o usuário pode ajustar o termo antes de pesquisar.

## Funcionalidades

* Captura de foto com câmera e controle de permissão
* Recorte da imagem antes do OCR para reduzir ruído e aumentar a taxa de acerto
* OCR on device com ML Kit Text Recognition
* Pós-processamento do texto para focar no nome do medicamento

  * remoção de palavras comuns de rótulo
  * filtragem de lote, validade, unidades e trechos irrelevantes
  * seleção da linha mais provável via pontuação
* Edição manual do termo reconhecido
* Abertura automática de pesquisa no navegador com o termo final

## Tecnologias

* Kotlin
* Jetpack Compose
* Activity Result API
* CameraX (captura de imagem)
* FileProvider (Uri seguro para arquivo)
* Google ML Kit Text Recognition (standalone, on device)

## Objetivo

Validar uma implementação simples de OCR no Android usando ML Kit, mostrando o fluxo completo de captura, preparação da imagem e extração do texto, além de pequenas otimizações para melhorar a experiência do usuário.
