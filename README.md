# WFDtoMaudeExample
This repository contains information and code related to an example that showcases the specification of Workflow Nets with Data in Maude.

The structure of the repo is as follows:
* /example : contains the example files:
  * [wfd-nettypes.maude](/example/wfd-nettypes.maude) : the definition of data types and operations used for a general WFD-net
  * wfd-netstruct.maude : the structure of the WFD-net in our example
  * wfd.maude : contains the rewrite rules that describe the semantics of the WFD-net
  * wfd-preds.maude : contains the atomic propositions () used for verification 
  * wdf-check.maude : contains the formulas describibg data-flow erorrs 
  * wfd-run.maude : contains verification commands for all the data-flow errors for the example

In order to run the verification procedure for the example, cd the example directory and load  wfd-run.maude 


