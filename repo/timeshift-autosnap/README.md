# timeshift-autosnap
Script de instantâneo automático Timeshift que é um procedimento
antes da atualização do plug usando a chamada Pacman.

# Ferramentas
*  Cria instantâneos Timeshift com comentários exclusivos.
*  Exclui instantâneos antigos criados usando este script.
*  Gera automaticamente o grub se o plug grub-btrfs estiver instalado.
*  Pode ser um procedimento manual fazendo o procedimento do plug `timeshift-autosnap` com privilégios mais altos.
*  Autosnaphot pode ser temporariamente ignorado definindo a variável de ambiente
   SKIP_AUTOSNAP (por exemplo, `sudo SKIP_AUTOSNAP= pacman -Syu`)

# Opções de /etc/timeshift-autosnap.conf:
*  `skipAutosnap` - se definido como **true**, o script não será um procedimento.
*  `deleteSnapshots` - se definido como **false**, instantâneos antigos não serão excluídos.
*  `maxSnapshots` - define o número **máximo** de instantâneos antigos a serem mantidos.
*  `updateGrub` - se definido como **false**, as entradas do grub não serão geradas.
*  `snapshotDescription` - define **valor** usado para distinguir instantâneos criados usando timeshift-autosnap.

# Observações
*  Funciona tanto no modo `BTRFS` quanto no modo `RSYNC`.
*  Este script é feito em distros referentes em Arch ou Arch, mas se
   houver interesse, ele deve ser facilmente portado para outras
   distros.

# Contribuição
*  Todas as novas ideias e colaboradores são bem-vindos.
