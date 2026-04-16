<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <title>To-Do List Acadêmico</title>
    <style>
        /* 1. Estilização Base */
        body { font-family: sans-serif; background: #f4f4f4; padding: 20px; }
        .container { max-width: 400px; margin: auto; background: white; padding: 20px; border-radius: 8px; box-shadow: 0 2px 10px rgba(0,0,0,0.1); }
        
        /* 2. Área de Entrada (Simulação Visual) */
        .input-group { margin-bottom: 20px; border-bottom: 2px solid #eee; padding-bottom: 10px; }
        input[type="text"], select { width: 100%; padding: 8px; margin: 5px 0; border: 1px solid #ccc; border-radius: 4px; }

        /* 3. Lista de Tarefas */
        .task-list { list-style: none; padding: 0; }
        .task-item { display: flex; align-items: center; padding: 10px; border-radius: 4px; margin-bottom: 8px; border-left: 5px solid; }

        /* 4. Estilização Condicional por Prioridade (via Classes) */
        .alta { border-left-color: #ff4d4d; background: #ffe6e6; }
        .media { border-left-color: #ffa500; background: #fff5e6; }
        .baixa { border-left-color: #2ecc71; background: #eafaf1; }

        /* 5. Ação de Conclusão (Lógica CSS) */
        input[type="checkbox"]:checked + span {
            text-decoration: line-through;
            color: #888;
            opacity: 0.6;
        }
    </style>
</head>
<body>

<div class="container">
    <h2>Minhas Tarefas</h2>
    
    <div class="input-group">
        <input type="text" placeholder="Descrição da tarefa...">
        <select>
            <option>Prioridade Alta</option>
            <option>Prioridade Média</option>
            <option>Prioridade Baixa</option>
        </select>
        <button style="width: 100%; padding: 8px; cursor: pointer;">Adicionar (Visual)</button>
    </div>

    <ul class="task-list">
        <li class="task-item alta">
            <input type="checkbox">
            <span>Estudar Engenharia de Prompt</span>
        </li>

        <li class="task-item media">
            <input type="checkbox">
            <span>Revisar código HTML/CSS</span>
        </li>

        <li class="task-item baixa">
            <input type="checkbox">
            <span>Organizar pastas do projeto</span>
        </li>
    </ul>
</div>

</body>
</html>
