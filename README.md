# Auto_Fill
 Information filler

Este script Python automatiza o preenchimento de campos em um aplicativo usando a biblioteca `pyautogui`, além de utilizar `openpyxl` para ler os dados de um arquivo Excel e `pyperclip` para copiar dados para a área de transferência.

1. **Importação de Bibliotecas**:
   - `pyperclip`: Usada para copiar dados para a área de transferência.
   - `openpyxl`: Usada para trabalhar com arquivos Excel.
   - `pyautogui`: Usada para automatizar a interação com o teclado e o mouse.

2. **Definição da Função `preencher_campo(coordenadas, valor)`**:
   - Copia o valor para a área de transferência.
   - Clica nas coordenadas especificadas (posição na tela).
   - Cole o valor usando `Ctrl+V`.

3. **Carregamento do Arquivo Excel**:
   - O arquivo Excel 'produtos_ficticios.xlsx' é carregado usando `openpyxl`.
   - A planilha 'Produtos' é selecionada.

4. **Definição das Coordenadas dos Campos na Tela**:
   - Cada par de coordenadas representa a posição na tela onde o campo deve ser preenchido.

5. **Loop de Preenchimento dos Campos**:
   - Para cada linha na planilha, itera sobre os campos e suas coordenadas correspondentes.
   - Obtém o valor do campo na célula atual.
   - Chama a função `preencher_campo` para preencher o campo com o valor atual.
   - Se o índice do campo for 11 (indicando o campo "Tamanho"), verifica o valor e clica em uma posição específica com base nesse valor.

6. **Cliques Finais**:
   - Depois de preencher todos os campos, são realizados cliques adicionais em elementos finais na tela.

Esse script é útil para automatizar tarefas repetitivas de preenchimento de formulários em aplicativos, economizando tempo e minimizando erros humanos.
