# Resume Assistant

Este projeto é um assistente de IA projetado para otimizar o processo de busca de emprego e apoiar o desenvolvimento de carreira. Ele ajuda os usuários a definir seus objetivos de carreira, praticar para entrevistas e descobrir oportunidades de emprego relevantes.

## Funcionalidades

*   **Criação de Perfil Personalizado**: Responda a um questionário de personalidade para definir seus interesses de carreira, nível de experiência, estilo de trabalho preferido e soft skills.
*   **Mapeamento de Objetivos de Carreira**: Com base no seu perfil, o assistente identifica funções e caminhos de carreira alvo.
*   **Recomendações de Cursos**: Receba sugestões de cursos personalizadas para aprimorar suas habilidades e alinhar-se aos seus objetivos de carreira.
*   **Simulação de Entrevista**: Pratique suas habilidades de entrevista com um entrevistador conduzido por IA que fornece feedback.
*   **Assistência na Busca de Emprego**: Encontre vagas de emprego relevantes com base nos parâmetros de busca definidos.

## Tecnologias Utilizadas

*   **Python**: Linguagem de programação principal para a lógica do backend.
*   **IA/LLM**: (Presumido para simulação de entrevistas e recomendações, embora não explicitamente declarado nos arquivos lidos).
*   **Markdown**: Para armazenamento de dados do usuário e configuração.

## Como Começar

### Pré-requisitos

*   Python 3.x instalado.
*   (Quaisquer outras dependências seriam listadas aqui, se conhecidas).

### Executando o Assistente

1.  **Navegue até o diretório do projeto**:
    ```bash
    cd C:/Users/aninh/Desktop/resume
    ```
2.  **Execute o script principal da aplicação**:
    ```bash
    python main.py # Ou o script de entrada apropriado, se diferente
    ```
3.  **Siga as instruções na tela**: O assistente o guiará pelo processo, começando com o questionário de personalidade.

## Gerenciamento de Dados

Os dados do usuário, resultados do questionário e perfis gerados são armazenados no diretório `data/` usando arquivos Markdown:

*   `personality-quiz.md`: Armazena as respostas do questionário do usuário.
*   `user-profile.md`: Contém o perfil do usuário gerado e as funções alvo.
*   `course-recommendations.md`: Lista os cursos recomendados.
*   `interview-session.md`: Rastreia o progresso e o histórico das simulações de entrevista.
*   `job-search-results.md`: Armazena os resultados das buscas de emprego.

## Contribuição

(Esta seção normalmente incluiria diretrizes para contribuir com o projeto, se aplicável.)

## Licença

(Especifique a licença do projeto aqui.)
