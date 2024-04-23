<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Tabela Interativa</title>
    <style>
        table {
            border-collapse: collapse;
            width: 100%;
        }
        th, td {
            border: 1px solid #dddddd;
            text-align: left;
            padding: 8px;
        }
        tr:nth-child(even) {
            background-color: #f2f2f2;
        }
        tr:hover {
            background-color: #dddddd;
        }
    </style>
</head>
<body>

<h2>Tabela Interativa</h2>

<table id="tabela">
    <thead>
        <tr>
            <th>Coluna 1</th>
            <th>Coluna 2</th>
            <th>Coluna 3</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>Dado 1</td>
            <td>Dado 2</td>
            <td>Dado 3</td>
        </tr>
        <tr>
            <td>Dado 4</td>
            <td>Dado 5</td>
            <td>Dado 6</td>
        </tr>
        <!-- Adicione mais linhas conforme necessário -->
    </tbody>
</table>

<script>
    // Script para tornar a tabela interativa
    var table = document.getElementById('tabela');
    var rows = table.getElementsByTagName('tr');
    for (var i = 0; i < rows.length; i++) {
        rows[i].addEventListener('click', function() {
            if (this.style.backgroundColor === '' || this.style.backgroundColor === 'white') {
                this.style.backgroundColor = '#ffcccc';
            } else {
                this.style.backgroundColor = 'white';
            }
        });
    }
</script>

</body>
</html>
