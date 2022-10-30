assembly-ai-plus
================

<!-- WARNING: THIS FILE WAS AUTOGENERATED! DO NOT EDIT! -->

> Simple Library for transcribing and understanding audio and video
> files using AssemblyAI.

Read more about AssemblyAI 👉 [Docs](https://www.assemblyai.com/docs)

## Install

``` sh
pip install assembly-ai-plus
```

## How to use

This Library provides a
[`AssemblyAI`](https://afizs.github.io/assembly-ai-plus/assemblyai.html#assemblyai)
class using which you can submit audio files for transcribing and
understanding.

``` python
from assembly_ai_plus.assemblyai import AssemblyAI
```

First create the assembly_ai instance by providing the AssemblyAI API
KEY, which you can get it for free from
[here](https://app.assemblyai.com/)

``` python
assembly_ai = AssemblyAI(api_key='YOUR_API_KEY')
```

### Submit the audio url for transcription

``` python
res = assembly_ai.submit_url_for_transcription(audio_url="https://bit.ly/3yxKEIY")
```

``` python
res.get('id') # This id is used to extract the actual text from the audio files.
```

    'rs3c8julbq-177d-4071-ab6f-d7c7a9bb6dbb'

### Getting the Transcription Result

``` python
full_details = assembly_ai.get_transcription_results('rs3c8julbq-177d-4071-ab6f-d7c7a9bb6dbb')
```

``` python
print(full_details['text'])
```

    You know, demons on TV like that. And and for people to expose themselves to being rejected on TV or, you know, humili humiliated by Fear Factor or, you know.

We can check out other details like sentiment analysis from
`full_details`
