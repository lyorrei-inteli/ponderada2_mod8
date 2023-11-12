# Navegação com Turtlebot usando ROS

## Introdução
Este repositório contém um pacote ROS desenvolvido para interagir programaticamente com o stack de navegação usando o Turtlebot 3, aplicável tanto em ambientes simulados quanto reais. O foco principal é em mapeamento e navegação autônoma.

## Instalação
### Pré-requisitos
- ROS2 Humble
- Gazebo (para simulação)
- Pacote Turtlebot 3
- Pacote Navigation2

### Configuração
Instruções detalhadas para configurar o ambiente ROS2 e instalar todas as dependências necessárias.

Navegue até a raiz do projeto e execute o seguinte comando para fazer a build dos pacotes:
```bash
colcon build
```

Depois, execute o seguinte comando (se estiver utilizando zsh mude o final do comando):
```bash
source install/local_setup.bash
```

## Uso
### Mapeamento
Instruções para iniciar o processo de mapeamento, incluindo o comando para ativar o mapeamento.

```bash
ros2 launch turtlebot3_nav_mapper turtlebot3_mapper_launch.xml
```

### Navegação
Instruções para iniciar a navegação, incluindo o comando para ativar a navegação.

```bash
ros2 launch turtlebot3_nav turtlebot3_nav_launch.xml
```

## Demonstração
Link para os vídeos no YouTube mostrando o sistema em funcionamento, cobrindo tanto o processo de mapeamento quanto a navegação.

### Mapeamento
https://youtu.be/7_cTNpSAFL0

### Navegação programática
https://youtu.be/vn11Je38uJI

### Teste de Navegação usando o software
https://youtu.be/rknkGxJ9fcA

## Funcionalidades

1. **Mapeamento Fidedigno**: 
   - O sistema é capaz de mapear ambientes de forma precisa e detalhada, seja em simulação ou com um Turtlebot 3 real. 
   - Utiliza sensores e algoritmos avançados para criar mapas confiáveis que servem de base para a navegação autônoma.

2. **Navegação Programática em Ambiente Pré-Mapeado**: 
   - Após o mapeamento, o sistema permite a navegação autônoma dentro do ambiente mapeado. 
   - A navegação é realizada através de comandos programáticos, permitindo que o Turtlebot 3 siga rotas pré-definidas ou reaja a comandos em tempo real.

3. **Desvio de Obstáculos Dinâmicos**:
   - O sistema não apenas segue o mapa previamente criado, mas também é capaz de identificar e desviar de obstáculos não mapeados que apareçam em seu caminho.
   - Esta funcionalidade aumenta a segurança e a adaptabilidade do Turtlebot 3 em ambientes dinâmicos, onde obstáculos podem surgir ou mudar de posição.
