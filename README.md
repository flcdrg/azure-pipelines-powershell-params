# Azure Pipelines PowerShell tasks with parameters

Trying to pass parameters to PowerShell script tasks in Azure Pipelines that use the [`param` keyword](https://learn.microsoft.com/powershell/module/microsoft.powershell.core/about/about_functions?view=powershell-7.4&WT.mc_id=DOP-MVP-5001655#functions-with-parameters).

TL;DR

[AzureCLI@2](https://learn.microsoft.com/azure/devops/pipelines/tasks/reference/azure-cli-v2?view=azure-pipelines&WT.mc_id=DOP-MVP-5001655) is the only one of the three tasks that allows you to pass parameters in via the `arguments` property.

The arguments property must be a single-line string, so use the `>` block style in your YAML if you want to split it over multiple lines.
