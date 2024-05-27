# Sales 



## Sales and Invoicing Workflow

1. **Sale Entry:**
    - A sale entry represents the sale of a product or service from the catalog to a customer. It can encompass various entities such as subscriptions, support tickets, or project tasks.

2. **Associating a Sale with Receivables:**
    - For a sale to be invoiced, it needs to be associated with a "receivable." A receivable represents an amount that is yet to be received, with information identifying the sale linked to it.

3. **Queuing for Invoicing:**
    - To initiate the invoicing process, receivables are queued in a receivable queue. This queue ensures orderly processing of receivables for invoicing.

4. **Receivable States:**
    - **Pending:** Receivables in this state are in draft form, awaiting further processing.
    - **Invoiced:** Once invoiced, the receivable moves to this state, indicating that it has been processed for billing.
    - **Cancelled:** Receivables can be cancelled, typically if the associated sale is voided or cancelled.

5. **Invoicing:**
    - Once a receivable is invoiced, it corresponds to a line item on a specific invoice.

**Example Workflow:**

1. A sale entry is recorded in the system, indicating the sale of a product or service.
2. The sale entry is associated with a receivable, representing the amount to be received.
3. The receivable is queued in the receivable queue.
4. Receivables are processed from the queue, moving from pending to invoiced state upon successful invoicing.
5. Invoiced receivables are reflected as line items on invoices generated for customers.

This workflow ensures efficient management of sales and invoicing processes within the system, providing clarity and accountability at each stage of the transaction lifecycle.



## Time tracker

### Sale Models

Sale Models are used to specify which pricing is applicable for the services of a given project.

A project is always assigned to a Sale Model, and there is a default Sale Model available.

In cases where different prices need to be applied on entries for the same client, it is necessary to create separate projects associated with different Sale Models.





Note nomenclature :
* "billing" : changement de département / responsabilité (l'encodage est terminé et validé, on peut passer à la facturation)
* "invoice": relatif aux finances et à l'émission de facture