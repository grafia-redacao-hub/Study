GRAFIA STUDY — PACOTE PWA

Arquivos
- index.html: aplicação Grafia Study
- manifest.webmanifest: metadados de instalação
- service-worker.js: cache da interface para uso offline básico
- icons/: ícones da aplicação

Como testar corretamente
1. Publique TODOS os arquivos preservando a estrutura de pastas em um host HTTPS.
2. Abra a URL publicada no Chrome/Edge (computador/Android) ou Safari (iOS).
3. No Android/desktop, use o convite nativo de instalação quando o navegador o exibir.
4. No iPhone/iPad, use Compartilhar > Adicionar à Tela de Início.

A instalação não pode ser validada abrindo index.html diretamente como arquivo local. Progressive Web Apps precisam ser servidos por HTTPS (localhost é exceção para desenvolvimento). O pacote não inclui servidor ou sincronização de conta.

Armazenamento
A aplicação preserva seus dados no localStorage do navegador/origem. Não existe sincronização entre dispositivos. Os dados locais do navegador e da versão instalada podem não ser compartilhados com outra origem; exporte JSON em Configurações antes de trocar a hospedagem.

Offline
O service worker armazena o shell da interface e os ícones. Como esta versão não depende de APIs externas, a interface pode abrir a partir do cache depois da primeira carga bem-sucedida. Os dados de estudo ficam em armazenamento local da origem. A primeira instalação e atualizações dependem de acesso à rede.
