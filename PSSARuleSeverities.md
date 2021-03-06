# DSC Resource Kit PSSA Rule Severities

**This list does not apply for tests and examples.**  
PSSA rules may be suppressed for tests and examples on a case-by-case basis.

## Must Pass
All DSC Resources must pass these rules.  
They are not allowed to be suppressed.

| Rule Name | PSSA Type | Why Error? |
|-----------|-----------|------------|
| PSAvoidDefaultValueForMandatoryParameter | Warning | This indicates an incorrect use of PowerShell. Default mandatory parameters will be overwritten by the user. |
| [PSAvoidDefaultValueSwitchParameter](https://github.com/PowerShell/PSScriptAnalyzer/blob/development/RuleDocumentation/AvoidDefaultTrueValueSwitchParameter.md) | Warning | This indicates an incorrect use of PowerShell. Switch parameters should always default to 'not provided'. |
| [PSAvoidInvokingEmptyMembers](https://github.com/PowerShell/PSScriptAnalyzer/blob/development/RuleDocumentation/AvoidInvokingEmptyMembers.md) | Warning | Extra empty members can make code confusing and messy. |
| [PSAvoidNullOrEmptyHelpMessageAttribute](https://github.com/PowerShell/PSScriptAnalyzer/blob/development/RuleDocumentation/AvoidNullOrEmptyHelpMessageAttribute.md) | Warning | This indicates an incorrect use of PowerShell. The HelpMessage attribute should not be provided if it is null or empty. |
| [PSAvoidUsingCmdletAliases](https://github.com/PowerShell/PSScriptAnalyzer/blob/development/RuleDocumentation/AvoidAlias.md) | Warning | Alias's may change hence the presence of an alias makes code potentially unstable. The base cmdlet should be used instead. |
| [PSAvoidUsingComputerNameHardcoded](https://github.com/PowerShell/PSScriptAnalyzer/blob/development/RuleDocumentation/AvoidUsingComputerNameHardcoded.md) | Error | Harcoding the computer name reveals sensitive system information. In addition, DSC Resources should be able to run on computers with any name. |
| [PSAvoidUsingDeprecatedManifestFields](https://github.com/PowerShell/PSScriptAnalyzer/blob/development/RuleDocumentation/AvoidUsingDeprecatedManifestFields.md) | Warning | All manifests should stay updated with the correct manifest fields. |
| [PSAvoidUsingEmptyCatchBlock](https://github.com/PowerShell/PSScriptAnalyzer/blob/development/RuleDocumentation/AvoidEmptyCatchBlock.md) | Warning | This indicates an incorrect use of PowerShell. Catch blocks should not be provided if empty. |
| [PSAvoidUsingInvokeExpression](https://github.com/PowerShell/PSScriptAnalyzer/blob/development/RuleDocumentation/AvoidUsingInvokeExpression.md) | Warning | Invoke-Expression is vulnerable to string injection. |
| [PSAvoidUsingPositionalParameters](https://github.com/PowerShell/PSScriptAnalyzer/blob/development/RuleDocumentation/AvoidUsingPositionalParameters.md) | Info | Named parameters should be used instead. |
| [PSAvoidShouldContinueWithoutForce](https://github.com/PowerShell/PSScriptAnalyzer/blob/development/RuleDocumentation/AvoidShouldContinueWithoutForce.md) | Warning | If ShouldContinue is used, it should be used correctly with the Force parameter. |
| [PSAvoidUsingUsernameAndPasswordParams](https://github.com/PowerShell/PSScriptAnalyzer/blob/development/RuleDocumentation/AvoidUsingUsernameAndPasswordParams.md) | Error | This is not secure. Use PSCredentials instead. |
| [PSAvoidUsingWMICmdlet](https://github.com/PowerShell/PSScriptAnalyzer/blob/development/RuleDocumentation/AvoidUsingWMICmdlet.md) | Warning | The author should use CIM cmdlets instead to comply with WSMan standards. |
| [PSAvoidUsingWriteHost](https://github.com/PowerShell/PSScriptAnalyzer/blob/development/RuleDocumentation/AvoidUsingWriteHost.md) | Warning | Write-Verbose should be used instead. |
| [PSDSCReturnCorrectTypesForDSCFunctions](https://github.com/PowerShell/PSScriptAnalyzer/blob/development/RuleDocumentation/ReturnCorrectTypeDSCFunctions.md) | Info | Required for the resource to work. |
| [PSDSCStandardDSCFunctionsInResource](https://github.com/PowerShell/PSScriptAnalyzer/blob/development/RuleDocumentation/UseStandardDSCFunctionsInResource.md) | Error | Required for the resource to work. |
| [PSDSCUseIdenticalMandatoryParametersForDSC](https://github.com/PowerShell/PSScriptAnalyzer/blob/development/RuleDocumentation/UseIdenticalMandatoryParametersDSC.md) | Error | Required for the resource to work. |
| [PSDSCUseIdenticalParametersForDSC](https://github.com/PowerShell/PSScriptAnalyzer/blob/development/RuleDocumentation/UseIdenticalParametersDSC.md) | Error | Required for the resource to work. |
| PSMisleadingBacktick | Warning | Extra backticks are not neccessary and indicate that the code is not clean. |
| [PSMissingModuleManifestField](https://github.com/PowerShell/PSScriptAnalyzer/blob/development/RuleDocumentation/MissingModuleManifestField.md) | Warning | All manifests should stay updated with the correct manifest fields. |
| [PSShouldProcess](https://github.com/PowerShell/PSScriptAnalyzer/blob/development/RuleDocumentation/UseShouldProcessCorrectly.md) | Warning | If you are using ShouldProcess, it should be used correctly. |
| [PSPossibleIncorrectComparisonWithNull](https://github.com/PowerShell/PSScriptAnalyzer/blob/development/RuleDocumentation/PossibleIncorrectComparisonWithNull.md) | Warning | $null should *always* be on the left side of comparisons in PowerShell in case the item you are comparing $null against is an array, may be an array in the future, or turns into an array due to an error. |
| [PSProvideCommentHelp](https://github.com/PowerShell/PSScriptAnalyzer/blob/development/RuleDocumentation/ProvideCommentHelp.md) | Info | All exported functions should be documented with comment help. |
| [PSReservedCmdletChar](https://github.com/PowerShell/PSScriptAnalyzer/blob/development/RuleDocumentation/AvoidReservedCharInCmdlet.md) | Warning | This indicates that the code won't run. |
| [PSReservedParams](https://github.com/PowerShell/PSScriptAnalyzer/blob/development/RuleDocumentation/AvoidReservedParams.md) | Warning | Reserved params are *reserved*. Don't redefine them. |
| [PSUseApprovedVerbs](https://github.com/PowerShell/PSScriptAnalyzer/blob/development/RuleDocumentation/UseApprovedVerbs.md) | Warning | Authors must follow PowerShell best practices by using only approved verbs. |
| [PSUseCmdletCorrectly](https://github.com/PowerShell/PSScriptAnalyzer/blob/development/RuleDocumentation/UseCmdletCorrectly.md) | Warning | This indicates that the author did not provide parameters required for a cmdlet. |
| [PSUseOutputTypeCorrectly](https://github.com/PowerShell/PSScriptAnalyzer/blob/development/RuleDocumentation/UseOutputTypeCorrectly.md) | Info | This ensures that all functions always return the correct types. |

## Flag - Occasionally can be overruled with approval
DSC Resources *should* pass these rules, but there are cases where these rules are allowed to be suppressed.

| Rule Name | PSSA Type | Cases Where Rule Supression Approved |
|-----------|-----------|--------------------------------------|
| [PSAvoidGlobalVars](https://github.com/PowerShell/PSScriptAnalyzer/blob/development/RuleDocumentation/AvoidGlobalVars.md) | Warning | <ul><li> Setting $global:DSCMachineStatus = 1 to trigger a machine reboot. </li></ul> |
| [PSAvoidUsingConvertToSecureStringWithPlainText](https://github.com/PowerShell/PSScriptAnalyzer/blob/development/RuleDocumentation/AvoidUsingConvertToSecureStringWithPlainText.md) | Error | <ul><li> Some resources may have outside dependencies that require conversion with plaintext. </li></ul> |
| [PSAvoidUsingPlainTextForPassword](https://github.com/PowerShell/PSScriptAnalyzer/blob/development/RuleDocumentation/AvoidUsingPlainTextForPassword.md) | Warning | <ul><li> Some resources may have outside dependencies that require insecure plaintext passwords. </li></ul> |
| PSDSCUseVerboseMessageInDSCResource | Info | <ul><li> A helper function is called which in turn calls Write-Verbose. </li></ul> |
| [PSUseDeclaredVarsMoreThanAssigments](https://github.com/PowerShell/PSScriptAnalyzer/blob/development/RuleDocumentation/UseDeclaredVarsMoreThanAssignments.md) | Warning | <ul><li> The variable is used on the same line as its assignment. </li><li> The variable is an approved global or environment variable. </li></ul> |
| [PSUsePSCredentialType](https://github.com/PowerShell/PSScriptAnalyzer/blob/development/RuleDocumentation/UsePSCredentialType.md) | Warning | <ul><li> Some resources may have outside dependencies that require string credentials. </li></ul> |

## Ignore
These rules will not be run on DSC resources and can be ignored.
They do not need to be suppressed.

| Rule Name | PSSA Type | Why Ignored? |
|-----------|-----------|--------------|
| [PSDSCDscExamplesPresent](https://github.com/PowerShell/PSScriptAnalyzer/blob/development/RuleDocumentation/DscExamplesPresent.md) | Info | High quality resources **must** have examples, but this rule doesn't correctly test this. |
| [PSDSCDscTestsPresent](https://github.com/PowerShell/PSScriptAnalyzer/blob/development/RuleDocumentation/DscTestsPresent.md) | Info | High quality resources **must** have tests, but this rule doesn't correctly test this. |
| [PSUseBOMForUnicodeEncodedFile](https://github.com/PowerShell/PSScriptAnalyzer/blob/development/RuleDocumentation/UseBOMForUnicodeEncodedFile.md) | Warning | There is already a test in place to ensure that all files except the mofs are not in Unicode. The mofs must be in ASCII. |
| [PSUseShouldProcessForStateChangingFunctions](https://github.com/PowerShell/PSScriptAnalyzer/blob/development/RuleDocumentation/UseShouldProcessForStateChangingFunctions.md) | Warning | This will trigger for Set-TargetResource which actually should not have ShouldProcess in this case. DSC Resources need to be able to run remotely without user confirmation or overrides. |
| [PSUseSingularNouns](https://github.com/PowerShell/PSScriptAnalyzer/blob/development/RuleDocumentation/UseSingularNouns.md) | Warning | Fixing this rule can make function names inaccurate and usually does not result in improved code. |
| [PSUseToExportFieldsInManifest](https://github.com/PowerShell/PSScriptAnalyzer/blob/development/RuleDocumentation/UseToExportFieldsInManifest.md) | Warning | We currently approve of using '*' for these fields in the module manifests since the exported members are often in flux due to the open source nature of the Resource Kit. |
| PSUseUTF8EncodingForHelpFile | Warning | DSC Resources do not have help files. |
