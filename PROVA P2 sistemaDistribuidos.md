
# Aluno: Luis Felipe Cardoso

# EVIDÊNCIA 1

![Evidência 1](https://github.com/user-attachments/assets/3716bc21-05ae-4b9a-801e-61669fe8f8cd)

## Problema A — Controle de Concorrência

MAXIMO_SIMULTANEO = 2

Foi alterado de número 3 para 2.

![Evidência 2](https://github.com/user-attachments/assets/92687f04-cdda-4cbf-a766-5c4d15101246)

# REPLICAÇÃO E CONSISTÊNCIA

## Problema B

def sincronizar():

    replica["estoque"] = principal["estoque"]

Foi alterado de réplica para principal.

![Evidência 3](https://github.com/user-attachments/assets/c0b8f5f5-a085-4e5b-b970-c52f0efba4c3)

# TOLERÂNCIA A FALHAS

## Problema C

if replica["online"]:

Foi alterado de principal para réplica.

![Evidência 4](https://github.com/user-attachments/assets/a2f6163b-21b2-455c-b88b-147005cde417)

# QUESTÕES

**1.** O semáforo limita a quantidade de threads que podem ser executadas simultaneamente, evitando sobrecarga.

**2.** É necessário porque, caso o servidor principal caia, a réplica entra para substituí-lo, mesmo estando desatualizada.

**3.** Significa que, caso ocorram falhas, o código continuará sendo executado por meio da réplica.

**4.** Serve para que somente uma thread modifique o estoque por vez, evitando erros.

**5.** É necessário atualizar o valor do estoque:

1. Os pedidos são processados no servidor principal.
2. O estoque é alterado conforme os pedidos realizados.
3. Após essa atualização, a sincronização envia o novo valor para a réplica.

# CONCLUSÃO

Com essa prova, aprendi a ler o código, identificar e corrigir os problemas solicitados e entender como funciona uma réplica caso o servidor principal apresente falhas.
