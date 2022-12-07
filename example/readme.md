
The example depicts a WFD-net modelling the processing of a mortgage application in
a bank. 

![Alt text](Img/wfd.png?raw=true "Title")

The data elements involved are: D = {c, chr, f, le, rn, cd}. 

The data element available (defined) when the process starts is the client application
data (c) - which includes the client personal information,
property information, client debts, income etc;

Transition *ra* (receive application) performs a read operation on *c*. After the execution of *ra*, two actions will be executed
in parallel: *ple* (provide loan estimate) - the
client is provided with a loan estimate (the data element
*le* is written) which details the estimated closing
costs and the monthly payment; *cch* (check credit history):
the loan officer will check the clients’ credit
history, providing a report (*chr*). After *cch*, if predicate
*okCHR(chr)* is false, a rejection notice is sent to
the client (*srj*), explaining the reason for the rejection
of the application. The data element *rn* (rejection
notice) is written. If *okCHR(chr)* is true, *pmf* (prepare
mortgage file) is executed: a loan officer verifies
all the information provided by the client, adding additional
information (title search, tax transcripts etc)
and prepares a file: the data element *f* is written and
*r*, *chr* are read. The next action, *rmf* (review mortgage
file), is performed by another employee who
reviews the file (*f* is read) and updates it with additional
data (*f* is written again). The action *scd* (send
closing documents) will be executed if the predicate
*okData(f ,chr)* is true (the loan is approved). In this
case, a set of closing documents (*cd*), will be written
and sent to the client for signing and the workflow terminates.
Data elements *f* and *chr* are deleted, as they
are no longer needed. If the predicate is false, the action
*rja* (reject application) is performed: a rejection
notice (*rn*) is written and *f* and *chr* are deleted.
