CTOS Watch Dogs Boot Animation — Pettyl

Módulo Magisk que troca a boot animation de sistema pela tela de "boot" do CTOS, no estilo da franquia **Watch Dogs**, feito para o **Motorola Moto E5 Play GO** (codinome `pettyl`).

![Preview da boot animation](preview.gif)

Sobre

Esse módulo substitui o `bootanimation.zip` do sistema por uma animação em vídeo com a estética do CTOS: barras de carregamento estilo "glitch", o texto `System Loading` e o logo em losango do CTOS.

Diferente da maioria dos módulos de boot animation (que usam uma sequência de PNGs com `desc.txt`), esse aqui usa o **formato de vídeo nativo da Motorola**, com `videodesc.txt` + arquivos `.mp4` — formato específico para telas que suportam boot animation em vídeo H.264 em vez de sprites.

Conteúdo do módulo

```
CTOS-WatchDogs-pettyl/
├── module.prop
└── system/
    └── media/
        └── bootanimation.zip
            ├── videodesc.txt      # descritor de reprodução (partes/loop)
            ├── 01_moto.mp4        # intro (480x960, ~16s, H.264)
            └── 02_loop.mp4        # loop de espera (480x960, ~0.7s, H.264)
```

> `sol.png` pode aparecer dentro do zip como resquício da versão anterior (que usava PNGs). No formato de vídeo atual ele não é referenciado pelo `videodesc.txt` — pode ser removido com segurança se quiser deixar o pacote mais limpo.

 Compatibilidade

- Testado no Motorola Moto E5 Play GO (pettyl)**.
- Depende do suporte da Motorola a boot animation em vídeo (`videodesc.txt` + `.mp4`). Aparelhos de outras marcas ou outros modelos Motorola que só leiam o formato clássico AOSP (`desc.txt` + PNGs) **não vão reproduzir corretamente** — nesse caso seria necessário reexportar a animação como sequência de imagens.

 Instalação

1. Baixe o `.zip` do módulo (release ou o próprio repositório).
2. Abra o app **Magisk** → aba **Módulos** → **Instalar do armazenamento**.
3. Selecione o `.zip` e aguarde a instalação.
4. Reinicie o aparelho.

**Requisitos:**
- Aparelho com **root via Magisk**.
- Bootloader desbloqueado (pré-requisito padrão pra instalar o Magisk).

 Créditos

- Estética e identidade visual do CTOS pertencem à franquia **Watch Dogs** (Ubisoft) — usada aqui apenas como referência/homenagem em um projeto pessoal, sem fins comerciais.
- Adaptação para o formato de vídeo da Motorola e empacotamento do módulo: [@teseeu](https://github.com/teseeu).

 Licença

Ainda sem licença definida.
