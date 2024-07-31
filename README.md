---

# ft_printf

Porque ft_putnbr() e ft_putstr() não são suficientes

## Resumo

O objetivo deste projeto é bastante direto. Você irá recodificar a função `printf()`. Você aprenderá principalmente sobre o uso de um número variável de argumentos. Que legal, não é mesmo? É realmente bastante legal :)

**Versão**: 10

## Conteúdos

- I Introdução
- II Instruções Comuns
- III Parte Obrigatória
- IV Parte Opcional
- V Submissão e Avaliação por Pares

---

### Capítulo I: Introdução

Você vai descobrir uma função popular e versátil em C: `printf()`. Este exercício é uma ótima oportunidade para melhorar suas habilidades de programação. É de dificuldade moderada.

Você descobrirá funções variáveis em C. A chave para um `ft_printf` bem-sucedido é um código bem estruturado e extensível. Após concluir esta tarefa, você poderá adicionar seu `ft_printf()` à sua libft para usá-lo em seus projetos escolares de C.

---

### Capítulo II: Instruções Comuns

- Seu projeto deve ser escrito em C.
- Seu projeto deve estar de acordo com a Norme. Se você tiver arquivos/funções bônus, eles são incluídos na verificação da norma e você receberá nota zero se houver um erro de norma.
- Suas funções não devem falhar inesperadamente (segfault, erro de bus, double free, etc.), exceto comportamentos indefinidos. Se isso acontecer, seu projeto será considerado não funcional e receberá nota zero durante a avaliação.
- Toda memória alocada no heap deve ser liberada corretamente quando necessário. Não serão tolerados vazamentos.
- Se o assunto exigir, você deve submeter um Makefile que compile seus arquivos fonte para a saída requerida com as flags `-Wall`, `-Wextra` e `-Werror`, usar `cc`, e seu Makefile não deve relinkar.
- Seu Makefile deve conter pelo menos as regras `$(NAME)`, `all`, `clean`, `fclean` e `re`.
- Para entregar bônus no seu projeto, você deve incluir uma regra `bonus` no seu Makefile, que adicionará todos os vários cabeçalhos, bibliotecas ou funções que são proibidos na parte principal do projeto. Os bônus devem estar em um arquivo separado `_bonus.{c/h}` se o assunto não especificar nada mais. A avaliação da parte obrigatória e bônus é feita separadamente.
- Se seu projeto permitir o uso da sua libft, você deve copiar seus fontes e seu Makefile associado para uma pasta `libft` com seu Makefile associado. O Makefile do seu projeto deve compilar a biblioteca usando seu Makefile, e depois compilar o projeto.
- Incentivamos você a criar programas de teste para seu projeto, mesmo que este trabalho não precise ser submetido e não será avaliado. Isso lhe dará a chance de testar facilmente seu trabalho e o trabalho dos seus colegas. Você achará esses testes especialmente úteis durante sua defesa. De fato, durante a defesa, você pode usar seus testes e/ou os testes do colega que está avaliando.
- Submeta seu trabalho no repositório git designado. Apenas o trabalho no repositório git será avaliado. Se o Deepthought for designado para avaliar seu trabalho, isso será feito após suas avaliações por pares. Se um erro ocorrer em qualquer seção do seu trabalho durante a avaliação do Deepthought, a avaliação será interrompida.

---

### Capítulo III: Parte Obrigatória

**Nome do Programa**: `libftprintf.a`

**Arquivos a serem entregues**: `Makefile`, `*.h`, `*/ *.h`, `*.c`, `*/ *.c`

**Makefile**: `NAME`, `all`, `clean`, `fclean`, `re`

**Funções externas autorizadas**: `malloc`, `free`, `write`, `va_start`, `va_arg`, `va_copy`, `va_end`

**Libft autorizada**: Sim

**Descrição**: Escreva uma biblioteca que contenha `ft_printf()`, uma função que irá imitar a função original `printf()`. Você deve recodificar a função `printf()` da libc.

O protótipo de `ft_printf()` é:
```c
int ft_printf(const char *, ...);
```

**Requisitos**:

- Não implemente o gerenciamento de buffer da `printf()` original.
- Sua função deve lidar com as seguintes conversões: `cspdiuxX%`.
- Sua função será comparada com a `printf()` original.
- Você deve usar o comando `ar` para criar sua biblioteca. O uso do comando `libtool` é proibido.
- Seu `libftprintf.a` deve ser criado na raiz do seu repositório.

**Conversões que você deve implementar**:

- `%c`: Imprime um único caractere.
- `%s`: Imprime uma string (conforme a convenção comum de C).
- `%p`: O argumento `void *` deve ser impresso em formato hexadecimal.
- `%d`: Imprime um número decimal (base 10).
- `%i`: Imprime um número inteiro em base 10.
- `%u`: Imprime um número decimal sem sinal (base 10).
- `%x`: Imprime um número em formato hexadecimal (base 16) em minúsculas.
- `%X`: Imprime um número em formato hexadecimal (base 16) em maiúsculas.
- `%%`: Imprime um sinal de porcentagem.

---

### Capítulo IV: Parte Opcional

Você não precisa fazer todos os bônus.

**Lista de Bônus**:

- Gerencie qualquer combinação dos seguintes flags: `'-0.'` e a largura mínima do campo em todas as conversões.
- Gerencie todos os seguintes flags: `'# +'` (Sim, um deles é um espaço).

Se você planeja completar a parte bônus, pense na implementação de seus recursos extras desde o início. Assim, você evitará os problemas de uma abordagem ingênua.

A parte bônus só será avaliada se a parte obrigatória estiver PERFEITA. Perfeito significa que a parte obrigatória foi integralmente feita e funciona sem falhas. Se você não passar TODOS os requisitos obrigatórios, sua parte bônus não será avaliada.
