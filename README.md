# Projeto de Reservas OutSystems - Traditional

<img width="831" height="640" alt="image" src="https://github.com/user-attachments/assets/f024bff7-e60f-403f-adcd-18120164625f" />

Este repositório contém um projeto de aplicação web para gestão de reservas de hotéis, desenvolvido inteiramente na plataforma de desenvolvimento low-code OutSystems. [cite_start]O objetivo da aplicação é fornecer uma ferramenta para a equipe do hotel gerenciar o ciclo de vida completo das reservas dos hóspedes, desde o agendamento até o check-out. [cite: 18]

## Funcionalidades da Aplicação

A aplicação de Reservas (Bookings) possui as seguintes funcionalidades:

* [cite_start]**Gestão de Quartos:** Permite criar, listar e editar os detalhes dos quartos do hotel, como número, capacidade de adultos/crianças e preço por noite. [cite: 171, 210]
* [cite_start]**Gestão de Comodidades (Amenities):** Funcionalidade para adicionar ou remover comodidades específicas (como Internet, TV, Cofre) de cada quarto. [cite: 410, 465]
* **Ciclo de Vida da Reserva:**
    * [cite_start]**Criação:** Permite registrar novas reservas, buscando o quarto mais barato disponível com base nas datas e no número de hóspedes. [cite: 277, 293, 321]
    * [cite_start]**Listagem e Filtro:** Exibe todas as reservas com a possibilidade de filtrar por sobrenome do hóspede e por status (Reservado, Check-In, etc.). [cite: 278, 354]
    * [cite_start]**Check-In, Check-Out e Cancelamento:** Ações para alterar o status de uma reserva [cite: 526, 527][cite_start], com regras de negócio que impedem, por exemplo, o cancelamento de uma reserva após o check-in. [cite: 542, 543]
* [cite_start]**Homepage (Dashboard):** Tela inicial que apresenta listas dinâmicas de hóspedes com check-in e check-out previstos para o dia, facilitando as operações diárias da recepção. [cite: 576, 600, 604]
* [cite_start]**Cobrança no Check-Out:** Ao fazer o check-out, o sistema apresenta uma tela de confirmação que calcula o custo total da estadia [cite: 546][cite_start], somando as diárias [cite: 573] [cite_start]e os serviços de quarto. [cite: 1175]
* [cite_start]**Serviço de Quarto:** Permite que os funcionários registrem cobranças de serviço de quarto (ex: lavanderia, bar) diretamente na reserva do hóspede. [cite: 1139, 1163]
* [cite_start]**Relatório de Ocupação:** Exibe um gráfico na homepage com a taxa de ocupação do hotel para os próximos 7 dias. [cite: 1079, 1080]

## Recursos da Plataforma OutSystems Utilizados

Este projeto foi construído explorando diversos recursos essenciais da plataforma OutSystems:

* **Modelagem de Dados:**
    * [cite_start]Criação de **Entidades** para armazenar dados (ex: `Room`, `Booking`). [cite: 91]
    * [cite_start]Uso de **Entidades Estáticas** para dados imutáveis (ex: `Status`, `Amenity`). [cite: 118, 411]
    * [cite_start]Definição de **Relacionamentos** entre entidades para garantir a integridade dos dados. [cite: 245, 247]
* **Interface e UI (Interface do Usuário):**
    * [cite_start]Construção de **Telas Web** para interação do usuário e uso de **Layouts** responsivos (`Layout_London`). [cite: 28, 160]
    * [cite_start]Reutilização de UI com **Web Blocks** para componentes como o nome do hóspede. [cite: 751]
    * [cite_start]Uso de **Formulários** para a entrada de dados nas telas de detalhes. [cite: 211, 295]
    * [cite_start]Aplicação de **Estilos (CSS)** para customizar a aparência da aplicação. [cite: 852, 889]
* **Lógica de Negócios:**
    * [cite_start]Implementação de **Server Actions** para encapsular regras de negócio reutilizáveis (ex: alterar status da reserva). [cite: 526]
    * [cite_start]Uso de **Agregados** [cite: 565] [cite_start]e **Queries SQL** [cite: 323] para consultar o banco de dados de forma otimizada.
* **Experiência do Usuário (UX):**
    * [cite_start]Uso de **AJAX** para atualizar partes da tela sem recarregar a página inteira, proporcionando uma experiência mais fluida. [cite: 716, 720, 724]
    * [cite_start]Utilização de **Variáveis de Sessão** para manter o estado dos filtros de busca entre as páginas. [cite: 798]
* **RichWidgets:**
    * [cite_start]Implementação de **Pop-ups** para ações em contexto, como a confirmação de check-out. [cite: 982, 984]
    * [cite_start]Uso de **Ícones** para melhorar a usabilidade visual dos cabeçalhos. [cite: 858]
    * [cite_start]Exibição de **Mensagens de Feedback** para informar o usuário sobre o sucesso ou falha de uma operação. [cite: 1055]
    * [cite_start]Adição de **Paginação** [cite: 1017] [cite_start]e **Ordenação** [cite: 1018] em listas longas para facilitar a navegação.
* **Segurança:**
    * [cite_start]Criação de **Perfis de Acesso (Roles)** para restringir o acesso a telas e funcionalidades específicas, como a exclusão de reservas. [cite: 766, 779, 786]
* **Visualização de Dados:**
    * [cite_start]Implementação de **Gráficos (Charts)** para exibir a taxa de ocupação do hotel de forma visual. [cite: 1079]

## Como Testar o Aplicativo

Para importar e testar este projeto no seu ambiente OutSystems, é necessário fazer o download dos dois arquivos de módulo (`.oml`) abaixo.

**Arquivos necessários:**

* `Breno_Booking.oml`
* `CloneOfBookings_core.oml`

Após o download, publique ambos os módulos em seu ambiente para poder executar e testar a aplicação completa.
