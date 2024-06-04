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

## Fundings

Fundings are a crucial element of financial management and serve as a mechanism for managing payments and due dates for sales.

They serve both to inform customers of expected amounts and to track payments received (or reimbursed), whether or not they are linked to specific invoices.

Here are the key features of Fundings and Funding plans : 

* **Communicating deadlines to customers:** Funding plans allow you to clearly communicate to customers the amounts to be paid and the associated due dates. This helps to improve transparency and avoid late payments.
* **Tracking payments received:** Funding plans allow you to track payments received, whether or not they are linked to specific invoices. This facilitates account reconciliation and cash flow management.
* **Managing split payments:** Funding plans can be used to manage split payments, which can be useful for large purchases or services spread over several months.
* **Adaptability to various use cases:** Funding plans can be generated in different ways, including through funding plans, balance invoices, or manually. This allows them to be adapted to a variety of use cases.

Fundings are meant to evolve over time (they can be modified and even deleted - as long as there is no associated payment).

**Funding plans** are a kind of assistance to create a series of Fundings at a given time, based on conditions related to the object for which the Fundings are issued.



Fundings can be generated:

* via a funding plan
* via a balance invoice
* in an arbitrary manner (programmatically or manually)



A distinction is made between:

* "funding_plan": used for specific services (e.g. Reservations)
* "payment_terms": used exclusively for invoices






## Time tracker

### Sale Models

Sale Models are used to specify which pricing is applicable for the services of a given project.

A project is always assigned to a Sale Model, and there is a default Sale Model available.

In cases where different prices need to be applied on entries for the same client, it is necessary to create separate projects associated with different Sale Models.





Note nomenclature :
* "billing" : changement de département / responsabilité (l'encodage est terminé et validé, on peut passer à la facturation)
* "invoice": relatif aux finances et à l'émission de facture