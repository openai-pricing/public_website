---
title: 'OpenAI Models'
date: 2024-08-12T06:48:15+02:00
draft: false
type: api
url: v0/openai-models
---

{{ $data := dict }}
{{ $p := "data/openai-models.json" }}
{{ with resources.Get $p }}
  {{ $data = . | transform.Unmarshal }}
{{ else }}
  {{ errorf "Unable to get resource %q" $p }}
{{ end }}
