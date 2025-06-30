# 📊 Diagramas PlantUML - Sistema VidaPlus

Este arquivo contém todos os diagramas UML do sistema VidaPlus em formato PlantUML, prontos para serem renderizados.

## 🎯 Diagramas Disponíveis

### 1. **Diagrama de Casos de Uso**
- **Arquivo:** `diagramas_plantuml.puml` (primeiro diagrama)
- **Descrição:** Mostra os atores e casos de uso do sistema
- **Atores:** Administrador, Médico, Enfermeiro, Recepcionista, Paciente
- **Casos de Uso:** 18 casos principais do sistema

### 2. **Diagrama de Classes**
- **Arquivo:** `diagramas_plantuml.puml` (segundo diagrama)
- **Descrição:** Estrutura de classes e relacionamentos
- **Classes Principais:** Usuario, Paciente, Consulta, Telemedicina, Faturamento
- **Enums:** StatusConsulta, TipoUsuario, FormaPagamento, etc.

### 3. **Diagrama de Atividades - Agendamento**
- **Arquivo:** `diagramas_plantuml.puml` (terceiro diagrama)
- **Descrição:** Fluxo completo do processo de agendamento
- **Processo:** Login → Seleção → Validação → Confirmação

### 4. **Diagrama de Atividades - Telemedicina**
- **Arquivo:** `diagramas_plantuml.puml` (quarto diagrama)
- **Descrição:** Fluxo de uma consulta de telemedicina
- **Processo:** Agendamento → Conexão → Consulta → Finalização

### 5. **Diagrama de Sequência - Login**
- **Arquivo:** `diagramas_plantuml.puml` (quinto diagrama)
- **Descrição:** Interação entre componentes durante o login
- **Participantes:** Usuario, Interface Web, Sistema de Autenticação, BD

### 6. **Diagrama de Estados - Consulta**
- **Arquivo:** `diagramas_plantuml.puml` (sexto diagrama)
- **Descrição:** Estados possíveis de uma consulta
- **Estados:** Agendada → Confirmada → Em Andamento → Finalizada

### 7. **Diagrama de Componentes**
- **Arquivo:** `diagramas_plantuml.puml` (sétimo diagrama)
- **Descrição:** Arquitetura de componentes do sistema
- **Pacotes:** Frontend, Backend, Banco de Dados, Serviços Externos

## 🛠️ Como Usar

### Opção 1: PlantUML Online
1. Acesse: https://www.plantuml.com/plantuml/uml/
2. Copie o código do diagrama desejado
3. Cole no editor online
4. O diagrama será gerado automaticamente

### Opção 2: VS Code com Extensão
1. Instale a extensão "PlantUML" no VS Code
2. Abra o arquivo `diagramas_plantuml.puml`
3. Use `Ctrl+Shift+P` e digite "PlantUML: Preview Current Diagram"
4. O diagrama será exibido em uma nova aba

### Opção 3: Plugin IntelliJ IDEA
1. Instale o plugin "PlantUML integration"
2. Abra o arquivo `.puml`
3. Clique com botão direito → "Preview Diagram"

### Opção 4: Plugin Eclipse
1. Instale o plugin "PlantUML"
2. Abra o arquivo `.puml`
3. O diagrama será renderizado automaticamente

## 📋 Comandos para Extrair Diagramas Individuais

### Para extrair apenas o Diagrama de Casos de Uso:
```bash
# Copie do início até @enduml do primeiro diagrama
sed -n '/@startuml "VidaPlus - Diagrama de Casos de Uso"/,/@enduml/p' diagramas_plantuml.puml > casos_uso.puml
```

### Para extrair apenas o Diagrama de Classes:
```bash
# Copie do segundo @startuml até @enduml
sed -n '/@startuml "VidaPlus - Diagrama de Classes"/,/@enduml/p' diagramas_plantuml.puml > classes.puml
```

## 🎨 Personalização

### Cores e Temas
Os diagramas usam um tema personalizado com cores do sistema VidaPlus:
- **Cor Primária:** #3b82f6 (Azul)
- **Cor de Fundo:** #f8fafc (Cinza claro)
- **Cor do Texto:** #1f2937 (Cinza escuro)

### Para alterar as cores:
```plantuml
skinparam backgroundColor #sua_cor_fundo
skinparam BorderColor #sua_cor_borda
skinparam FontColor #sua_cor_texto
```

## 📱 Exportação

### Formatos Suportados:
- **PNG:** Para uso em documentos
- **SVG:** Para web (escalável)
- **PDF:** Para impressão
- **EPS:** Para LaTeX

### Comando para exportar:
```bash
# PNG
plantuml -tpng diagramas_plantuml.puml

# SVG
plantuml -tsvg diagramas_plantuml.puml

# PDF
plantuml -tpdf diagramas_plantuml.puml
```

## 🔧 Configuração do PlantUML

### Pré-requisitos:
- Java Runtime Environment (JRE)
- Graphviz (para alguns tipos de diagrama)

### Instalação:
1. **Windows:** Baixe o JAR do PlantUML
2. **Mac:** `brew install plantuml`
3. **Linux:** `sudo apt-get install plantuml`

## 📝 Notas Importantes

1. **Compatibilidade:** Os diagramas são compatíveis com PlantUML versão 1.2023+
2. **Performance:** Diagramas complexos podem demorar alguns segundos para renderizar
3. **Navegadores:** Para uso online, recomenda-se Chrome ou Firefox
4. **Resolução:** Para melhor qualidade, exporte em alta resolução (300 DPI)

## 🎯 Uso no Documento Acadêmico

Para incluir os diagramas no seu documento:

1. **Gere as imagens** usando um dos métodos acima
2. **Inserir no Word/Google Docs** como imagens
3. **Adicionar legendas** explicativas
4. **Referenciar no texto** quando necessário

### Exemplo de referência:
```
"Conforme mostrado no Diagrama de Casos de Uso (Figura 1), o sistema possui cinco atores principais..."
```

## 🆘 Solução de Problemas

### Diagrama não renderiza:
- Verifique se o Java está instalado
- Confirme se o Graphviz está instalado (se necessário)
- Verifique a sintaxe do código PlantUML

### Erro de codificação:
- Salve o arquivo em UTF-8
- Use apenas caracteres ASCII quando possível

### Performance lenta:
- Divida diagramas muito grandes
- Use temas mais simples
- Considere usar cache local

---

**Criado por:** Jamim Magalhães Oliveira  
**Data:** [DATA ATUAL]  
**Versão:** 1.0 