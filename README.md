# Desafio Repositório Github
Treinamento prático de repositório Git-Github



GIT BÁSICO
==========

comandos Git:

1. Git BASH HERE > abre o Git na pasta do windows
2. git Init > inicializar (é criado na pasta o .git que está escondido)
3. git status > mostra o relatório dos arquivos que já foram ou não incluidos no controle de versão
4. git add "nome do arquico" > para adicionar um arquivo ao controle de versão
5. git add . > para adicionar todos os arquivos na pasta
6. git commit -m "commit inicial" > criar a primeira versão do código
7. caso não tenha configurado o seu email e nome use:
8. git config --global user.email "seu@email"
9. git config --global user.name "username"
10. definir o link do repositório na nuvem: criar um novo repositório no Github
11. copiar o endereço url do novo repositório criado
12. de volta no git usar: 
13. git remote add origin LINK DO REPOSITÓRIO
14. git push --set-upstream origin master > adicionar o projeto do desktop no repositório na nuvem
15. git status > relatório
16. entra no github e f5 pra checar se foi tudo certo
17. criou algum arquivo novo ou alterou?
18. git add "nome do arquivo" ou git add .
19. git status > relatorio
20. agora precisa fazer outro commit para segunda versão do codigo
21. git commit - m "descrição da mudança"
22. git push > enviar para o repositório a mudança
23. Volte ao Github e F5 para confirmação 
24. ==
25. git refolg > verificar o histórico de versões do código no repositório
26. a versão mais atual será a do topo da lista
27. ==
28. quer voltar para uma verão anterior?
29. git reset --hard (numero do id da versão)
30. git reflog > checa as versões novamente
31. caso queira voltar para outra versão repita o passo 29

GIT AVANÇADO
============
Criar branchs, mudar de branch, fazer Merge, Pull...

git branch > verificar as branchs
bit branch nome-da-nova-branch > criar uma branch nova para testes
git checkout nome-da-nova-branch > passar a trabalhar com essa branch
tudo que eu alterar e criar agora estará indo para a nova branch e não afetará a master

use git add para adicionar nesta branch
crie um commit com uma boa descrição e para fazer o push:
git push --set-upstream origin nome-da-nova-branch > adicionar a nova branch no repositório na nuvem
ir no github F5 e conferir a criação da nova branch

Os testes na nova branch funcionaram? quer passar os novos códigos para a branch principal estável?
ATENÇÂO! antes de fazer o merge você deve puxar as branchs da nuvem para o seu desktop
isso impede de fazer confusões com trabalho em equipe
git pull < fazer os downloads das branchs atualizadas da nuvem para seu desktop
aí sim você pode fazer a merge sem problemas

git merge > trazer as atualizações para a branch principal
git branch > verificar as branchs
git checkout master > ir para a master
git branch > checar se foi mesmo
git merge nome-da-nova-branch > trazer as alteraçoes da branch nova para a branch master
git push > mandar para a nuvem

outros comandos:
git checkout -b novaBranch master > criar uma nova branch com base na branch principal
git branch > checar se criou e se foi para a nova
já pode add e fazer commit nessa nova branch

testou o novo codigo e está funcionando? quer mergear na master?

git chackout master > ir para a master
git pull > fazer o pull da nuvem para seu desktop
git merge novaBranch > juntar o novo codigo na branch master estável
git push > enviar para a nuvem

PULL REQUEST
quando algum programador deve autorizar sua alteração de codigo
pelo próprio github voce faz a solicitação e escreve um comentário

Git ignore
quando acontece de você não querer mandar para a nuvem alguns arquivos ou pastas

touch .gitignore > cria um arquivo .txt 
nesse arquivo você escreve os arquivos ou pastas que vc não quer que sejam 
adicionados ao controle de versão
escreva no arquivo de texto o nome Diretorio/ ou o nome de um arquivo e salva.
pronto, agora o git irá ignorar essa pasta ou arquivo.
depois adiciona esse gitignore no projeto



