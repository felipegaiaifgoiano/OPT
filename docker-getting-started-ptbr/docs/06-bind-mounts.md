# Bind Mounts

**Progresso do tutorial:** 6 / 8

[🏠 Início](../README.md) | [◀ Anterior](05-persist-data.md) | [Próximo ▶](07-multi-container.md)

Bind mounts permitem compartilhar arquivos entre o host e o container.

Isso é muito útil durante o desenvolvimento.

---

## Executando com bind mount

```bash
docker run -dp 3000:3000 -v $(pwd):/app getting-started
```
---

## Próximo passo

Agora vamos executar múltiplos containers trabalhando juntos.

➡ Continue para [**07-multi-container.md**](07-multi-container.md)
