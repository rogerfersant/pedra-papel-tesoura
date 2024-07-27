import random

def jogo_pedra_papel_tesoura():
    opcoes = ['pedra', 'papel', 'tesoura']
    computador = random.choice(opcoes)

    escolha_usuario = input('Escolha pedra, papel ou tesoura: ').lower()

    if escolha_usuario not in opcoes:
        print('Escolha invalidade, tente novamente')
        return
    
    print(f'Computador escolheu: {computador}')

    if escolha_usuario == computador:
        print('Empate!')
    elif (escolha_usuario == 'pedra' and computador =='tesoura') or \
    (escolha_usuario == 'papel' and computador == 'pedra') or \
    (escolha_usuario == 'tesoura' and computador =='papel'):
        print('Você ganhou!')
    else:
        print('Você perdeu!')

jogo_pedra_papel_tesoura()

pergunta = input ('Deseja tentar mais uma vez?: ').lower()

if pergunta == 'sim':
    jogo_pedra_papel_tesoura()
else:
    print('Fim do jogo')
    
