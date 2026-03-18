# Instalação do Kompose

**Progresso:** 2 / 6

[🏠 Início](README.md) | [◀ Anterior](01-introducao.md) | [Próximo ▶](03-revisar-projeto.md)

---

## Conceito

O Kompose é uma ferramenta de linha de comando.

Ele deve ser instalado no seu sistema operacional para ser utilizado.

---

## Passo a passo

### MacOS

```bash
brew install kompose
```

### Linux

```bash
curl -L https://github.com/kubernetes/kompose/releases/download/v1.31.2/kompose-linux-amd64 -o kompose
chmod +x kompose
sudo mv kompose /usr/local/bin
```

### Windows

```bash
choco install kubernetes-kompose
```

---

## Observações

Para verificar se a instalação está correta, utilize:

```bash
kompose version
```

Se aparecer a versão, está tudo OK.