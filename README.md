O que é try-catch em programação?

Em linguagens como C#, o try-catch é um mecanismo usado para tratar erros que podem acontecer durante a execução do programa.

Ele funciona assim:

try → Onde você coloca o código que pode gerar erro
catch → Parte que “pega” o erro e impede que o programa quebre
finally (opcional) → Roda sempre, com ou sem erro

Exemplo simples:

try
{
    int numero = int.Parse("abc"); // isso dá erro
}
catch (Exception ex)
{
    Console.WriteLine("Ocorreu um erro! Entrada inválida.");
}

Sem try-catch → o programa trava
Com try-catch → o erro é tratado e o programa continua funcionando

Como o try-catch se conecta com a Prevenção de Erros

A 5ª Heurística de Nielsen — Prevenção de Erros diz que:

“A melhor interface é aquela que evita que o erro aconteça, e quando inevitável, ajuda o usuário a se recuperar sem trauma.”

O try-catch é uma ferramenta de programação que apoia diretamente a prevenção de erros no UX, porque:

✔ 1. Evita que o sistema quebre

Quando acontece algo inesperado (ex: usuário digita letra onde deveria ser número), o catch impede que o programa feche ou dê mensagem técnica estranha.

✔ 2. Substitui erros técnicos por mensagens compreensíveis

Em vez de aparecer: System.FormatException: Input string was not in a correct format
O sistema mostra:  Entrada inválida. Digite apenas números.

Isso é Prevenção de Erros → o sistema ajuda o usuário a não errar novamente.

✔ 3. Mantém o fluxo do usuário

Mesmo após um erro, o sistema não trava.
O usuário continua usando normalmente.

✔ 4. Permite criar mensagens educativas

A prevenção melhora quando você orienta o usuário dentro do catch: Console.WriteLine("Você digitou um valor inválido. Tente novamente usando apenas números.");

<img width="1366" height="768" alt="image" src="https://github.com/user-attachments/assets/a8bf4038-0df4-4aeb-bbd5-a884b3f47625" />

<img width="1366" height="768" alt="image" src="https://github.com/user-attachments/assets/ee40da61-7e8c-4d89-99bb-fbf30948af0b" />

