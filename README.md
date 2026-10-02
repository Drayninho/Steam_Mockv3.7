[README.md](https://github.com/user-attachments/files/32963268/README.md)
# Steam Inventory Mock v3.7

Mock visual/local para o inventário CS2 no cliente Steam via Millennium. Não cria nem altera itens no servidor.

## Mudanças desta versão
- Recarrega as imagens dos itens reais usando `g_ActiveInventory.LoadItemImage`, sem substituir o `src` dos itens reais.
- A seleção de uma skin falsa usa o próprio `g_ActiveInventory.SelectItem` com um `rgItem` sintético baseado em um item real.
- O Steam constrói o `inventory_iteminfo` nativo a partir desse objeto local; o plugin apenas corrige campos específicos após a construção.
- Não cria janela/painel de detalhes paralelo.
- A skin falsa continua ocupando um slot real da grade.

## Build
```powershell
bun install
bun run build
```
