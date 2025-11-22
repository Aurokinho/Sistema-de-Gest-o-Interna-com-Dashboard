# Sistema-de-Gest-o-Interna-com-Dashboard
Um sistema web simples que controla empréstimo e devolução de notebooks/acessórios, mostra dashboard com status em tempo real e gera relatório PDF — tudo no navegador, sem instalar nada.

  O projeto é um sistema web interno que acaba com a bagunça do controle de notebooks e acessórios feito no Excel.
Qualquer pessoa da empresa abre no navegador, faz login rapidinho, registra quem pegou ou devolveu o equipamento e já vê na hora quantos estão disponíveis, quem está atrasado e tudo mais num dashboard bonito.
Com um clique gera relatório em PDF pra auditoria ou pro chefe e pronto — nunca mais perde tempo procurando.

Como funciona no dia a dia :
O colaborador abre no navegador → faz login rápido → vê o dashboard com tudo atualizado.
Clica “Emprestar” ou “Devolver” → registra em 3 segundos.
O usuario abre, vê os números e gráficos → clica “Relatório” → sai PDF pronto.

As regras de negocio no me projeto é:

As regras de negócio são as “leis” que a empresa já segue na vida real. O sistema não pode deixar ninguém quebrar essas leis. No meu projeto eu garanti isso da seguinte forma:
1.  Só pode reservar/pegar se estiver livre O botão de “Pegar” ou “Reservar” só aparece quando o item está com status “Disponível”. Se já estiver com alguém, o botão desaparece ou aparece desativado.
2.  Todo empréstimo tem prazo máximo A empresa definiu: notebook = 30 dias, EPI = 365 dias, sala = mesmo dia. O sistema grava a data de saída automaticamente.
3.  Passou do prazo → muda sozinho para “Atrasado” ou “Vencido” Toda vez que alguém abre o sistema (ou à meia-noite), ele verifica automaticamente as datas. Se passou do prazo, muda a cor para vermelho e já conta como atrasado no dashboard.
4.  Impede ações erradas
	•  Não deixa devolver algo que já está disponível
	•  Não deixa pegar duas vezes o mesmo item
	•  Se tentar fazer algo errado, aparece um aviso simpático (“Este notebook já está com o João”).
5.  Grava quem fez e quando Cada movimento fica registado: quem pegou, quem devolveu, data e hora exata, e o nome de quem registrou no sistema.
6.  Dashboard sempre mostra a verdade do momento Os números grandes e os gráficos são recalculados em tempo real. O chefe abre e vê exatamente quantos estão livres, quantos estão emprestados e quantos estão atrasados – sem precisar clicar em nada.  




