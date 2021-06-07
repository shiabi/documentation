===========================
Process returns and refunds
===========================

The :guilabel:`Sales` app provides two different ways to process returns based on whether an
invoice has been sent or not.

Before invoicing: Reverse Transfers
===================================

Returns are completed using *Reverse Transfers* when a customer decides to return a product before
an invoice has been sent or validated.

.. note::
   In order to use Reverse Transfers, the :guilabel:`Inventory` app must also be installed.

To start a return, navigate to the customer's sales order, and click on the :guilabel:`Delivery`
smart button to open the associated delivery order.

On the validated delivery order, click :guilabel:`Return` to open the :guilabel:`Reverse Transfer`
pop-up window. By default, the :guilabel:`Quantity` matches the validated quantities from the
delivery order. Update the quantities if necessary. Click on the trash icon next to a line item to
remove it from the return.

.. image:: returns/reverse-transfer-popup.png
   :align: center
   :alt: Reverse Transfer Pop-Up

Click :guilabel:`Return` to confirm the return. This generates a new warehouse operation for the
incoming returned product(s). Upon receiving the return, the warehouse team *validates* the
warehouse operation. Then, on the original sales order, the :guilabel:`Delivered` quantity will
reflect the difference between the initial validated quantities and the returned quantities.

.. image:: returns/updated-sales-quantities.png
   :align: center
   :alt: Updated Sales Order Quantities

When an invoice is created, the customer receives an invoice only for the products they are
keeping.

After invoicing
===============

Sometimes, customers return an item after they receive and/or pay for their invoice. In these
cases, a return using only Reverse Transfers is impossible since validated or sent invoices cannot
be changed. But Reverse Transfers can be used in conjunction with *Credit Notes* to complete the
customer's return.

To start a return, navigate to the relevant sales order. If there is a payment registered on the
sales order, then the payment details will appear in the Chatter, and the invoice (accessible
through the :guilabel:`Invoices` smart button) will have a green banner across it.

From the sales order, click on the :guilabel:`Delivery` smart button to view the validated delivery
order. Then click :guilabel:`Return` to open the :guilabel:`Reverse Transfer` pop-up window. Edit
the :guilabel:`Product` or :guilabel:`Quantity` as needed for the return, then click
:guilabel:`Return`. This generates a new warehouse operation for the incoming returned product(s),
which is validated by the warehouse team once the return is received. Then, on the sales order, the
:guilabel:`Delivered` quantity will reflect the difference between the initial validated quantities
and the returned quantities.

.. image:: returns/case-2-updated-sales-quantities.png
   :align: center
   :alt: Updated Delivered Quantities

Since the returned products have already been paid for, the validated invoice must be modified to
reflect the return. Navigate to the relevant invoice (from the sales order, click on the
:guilabel:`Invoices` smart button). Then, click on the :guilabel:`i` icon next to the
:guilabel:`Paid` line at the bottom of the invoice to open the :guilabel:`Payment Info` window.
Click :guilabel:`Unreconcile`.

.. image:: returns/unreconcile-button.png
   :align: center
   :alt: Unreconcile Button

After the invoice is unreconciled, the options for :guilabel:`Send & Print` and
:guilabel:`Register Payment` become available again alongside a note that there are outstanding
payments for the customer.

To process a refund, click :guilabel:`Add Credit Note` from the validated invoice.

.. image:: returns/credit-note-popup.png
   :align: center
   :alt: Credit Note pop-up

Choose whether to issue a :guilabel:`Partial Refund`, :guilabel:`Full Refund`, or
:guilabel:`Full Refund and new draft invoice`. The :guilabel:`Partial Refund` option creates a
draft Credit Note that can be edited before posting. The
:guilabel:`Full Refund and new draft invoice` option validates the Credit Note and duplicates the
original invoice as a new draft.

A :guilabel:`Reason` for the credit and a :guilabel:`Specific Journal` to use to process the credit
can also be specified. If a :guilabel:`Specific Reversal Date` is selected, then a
:guilabel:`Refund Date` must also be selected.

Click :guilabel:`Reverse`. Then, for a :guilabel:`Partial Refund` or
:guilabel:`Full Refund and new draft invoice`, :guilabel:`Edit` the draft as needed, then
:guilabel:`Confirm`.

.. image:: returns/outstanding-payment-banner.png
   :align: center
   :alt: Outstanding payments banner