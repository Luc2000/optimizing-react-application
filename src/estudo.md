useMemo => Evita que calculos que resultam em valores pesados sejam refeitos toda vez que o componente renderizar, faz só quando 2° parâmetro satisfeito.
useCallback => Evita que FUNÇÕES sejam recriadas e por consequência, realocadas em memória, só faz só quando 2° parâmetro satisfeito.

useMemo explicação: 
    useMemo pode ficar em volta de uma função que calcula algo. 
    Como segundo parâmetro você pode passar a dependência do que faz ele atualizar.

    Ele é útil para ser utilizado quando:
    1. Existe um cálculo pesado que é feito muitas vezes pq o componente renderiza muitas vezes.
    2. Quando mesmo que pequeno, um cálculo ou mudança é repassada para algum compnente filho.

useCallback explicação:
    Quase igual ao useMemo, mas ele é mais para FUNÇÕES, memorizar funções e não VALORES igual o useMemo.
    Nós usamos o useCallback pela IGUALDADE REFERENCIAL dela. Ou seja, suponhamos que a função é usada em mais de um lugar... Não é bom recriá-la.