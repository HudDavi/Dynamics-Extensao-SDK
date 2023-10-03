# Aplicativo de Integração com Dynamics 365

## Visão Geral

Este é um projeto que demonstra como integrar e interagir com o Microsoft Dynamics 365 usando a biblioteca Microsoft.Xrm.Sdk. O aplicativo é escrito em C# e oferece funcionalidades para se conectar ao Dynamics 365, realizar consultas, criar, atualizar e excluir registros, bem como trabalhar com FetchXML.

## Pré-requisitos

Antes de começar a usar este aplicativo, certifique-se de que você tenha os seguintes requisitos:

- Visual Studio ou outra IDE C#.
- Biblioteca `Microsoft.Xrm.Sdk` e suas dependências.
- Microsoft Dynamics 365 ou ambiente compatível.
- Credenciais válidas para acessar o Dynamics 365.

## Configuração

### Arquivo de Configuração (app.config)

```xml
<?xml version="1.0" encoding="utf-8"?>
<configuration>
  <runtime>
    <assemblyBinding xmlns="urn:schemas-microsoft-com:asm.v1">
      <!-- Dependência: System.Runtime.CompilerServices.Unsafe -->
      <dependentAssembly>
        <assemblyIdentity name="System.Runtime.CompilerServices.Unsafe" publicKeyToken="b03f5f7f11d50a3a" culture="neutral" />
        <bindingRedirect oldVersion="0.0.0.0-6.0.0.0" newVersion="6.0.0.0" />
      </dependentAssembly>
      <!-- Dependência: System.Text.Json -->
      <dependentAssembly>
        <assemblyIdentity name="System.Text.Json" publicKeyToken="cc7b13ffcd2ddd51" culture="neutral" />
        <bindingRedirect oldVersion="0.0.0.0-6.0.0.2" newVersion="6.0.0.2" />
      </dependentAssembly>
      <!-- Dependência: Microsoft.Xrm.Sdk -->
      <dependentAssembly>
        <assemblyIdentity name="Microsoft.Xrm.Sdk" publicKeyToken="31bf3856ad364e35" culture="neutral" />
        <bindingRedirect oldVersion="0.0.0.0-7.0.0.0" newVersion="7.0.0.0" />
      </dependentAssembly>
    </assemblyBinding>
  </runtime>
</configuration>
```

### Pacotes NuGet (packages.config)

```xml
<?xml version="1.0" encoding="utf-8"?>
<packages>
  <package id="Microsoft.Bcl.AsyncInterfaces" version="6.0.0" targetFramework="net462" />
  <package id="Microsoft.CrmSdk.CoreAssemblies" version="9.0.2.45" targetFramework="net462" />
  <!-- Outras dependências do projeto -->
</packages>
```

## Uso

1. Clone ou faça o download deste repositório para a sua máquina local.
2. Abra o projeto em sua IDE C#.
3. Configure as credenciais e informações de conexão no método `ObterConexao` da classe `Conexao` para se conectar ao seu ambiente Dynamics 365.
4. Execute o aplicativo para testar as funcionalidades, como consulta, criação, atualização e exclusão de registros no Dynamics 365.

## Funcionalidades

O aplicativo oferece as seguintes funcionalidades:

- Consulta de registros usando FetchXML.
- Criação de registros no Dynamics 365.
- Atualização de registros existentes.
- Exclusão de registros.
- Manipulação de entidades do Dynamics 365.

## Licença

Este projeto é distribuído sob a licença MIT. Consulte o arquivo [LICENSE](LICENSE) para obter detalhes.

## Autor

- Hudson Silva