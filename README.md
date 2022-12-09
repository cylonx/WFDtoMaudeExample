# WFDtoMaudeExample
This repository contains information and code related to an example that showcases the specification of Workflow Nets with Data in Maude.

The structure of the repo is as follows:
* /example : contains the example files:
  * [wfd-nettypes.maude](/example/wfd-nettypes.maude) : the definition of data types and operations used for a general WFD-net
  * [wfd-netstruct.maude](/example/wfd-netstruct.maude) : the structure of the WFD-net in our example
  * [wfd.maude](/example/wfd.maude) : contains the rewrite rules that describe the semantics of the WFD-net
  * [wfd-pred.maude](/example/wfd-preds.maude) : contains the state predicates used for verification 
  * [wfd-check.maude](/example/wdf-check.maude) : contains the formulas describibg data-flow erorrs 
  * [wfd-run.maude](/example/wdf-run.maude) : contains verification commands for all the data-flow errors for the example
  * [lisiting.txt](/listing.txt) : contains a listing of the results obtained by running the commands in wfd-run


In order to run the verification procedure for the example, cd the example directory and load  wfd-run.maude 


