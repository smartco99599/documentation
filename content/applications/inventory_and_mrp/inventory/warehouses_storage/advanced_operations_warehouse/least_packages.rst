======================
Least packages removal
======================

The *least packages* removal strategy fulfills an order by opening the fewest number of packages,
ideal for maintaining organized stock without multiple open boxes.

To understand how the removal strategy works, consider how a warehouse stores packages of flour in
bulk. Purchased products are packaged in `10 kg`, `30 kg`, `50 kg`.

Then, the flour is stored in a sealed package in quantities of `100 kg`. To minimize moisture or
pests from entering open packages, the least packages removal strategy is used to pick from a
single, opened package.

.. example::
   A package of `100 kg` of flour is depleted to `54 kg` after fulfilling some orders. There are
   other packages of `100 kg` in stock.

   #. When an order for `14 kg` of flour is placed, the package of 54 kg is selected.
   #. However, if an order is placed for more than `54 kg` of flour, one of the packages of `100 kg`
      is used to fulfill the order.

Workflow
--------

To use the removal strategy, :ref:`enable the packages <inventory/removal/pack-setup>` feature.

To see how the least packages removal strategy works, consider the product, `Flour`, in the
following example. The product's :guilabel:`Units of Measure` field on the product form is set to
`kg`. The product is stored in packages of one hundred kilograms, with one package with `54 kg`
remaining.

.. tip::
   To check the product's on-hand stock, navigate to the product form and click the :guilabel:`On
   Hand` smart button.

   .. image:: least_packages/on-hand-flour.png
      :align: center
      :alt: Show on-hand stock in each package.

Navigate to the product category, `Wheats`, and set the :guilabel:`Force Removal Strategy` to
:guilabel:`Least Packages`.

.. seealso::
   :ref:`Set removal strategy on product category <inventory/routes/strategies/set>`

.. image:: least_packages/set-least-packages.png
   :align: center
   :alt: Set least packages removal strategy on the product category.

Create a :ref:`delivery order <inventory/delivery/one-step>` for eighty kilograms of flour, either
by going to the :menuselection:`Sales app` and creating a new quotation, or from the delivery orders
dashboard in :menuselection:`Inventory --> Operations --> Deliveries`.

On the delivery order, the :guilabel:`Quantity` field displays the amount automatically picked
according to the removal strategy. For more details about *where* the units were picked, select the
:guilabel:`⦙≣ (bulleted list)` icon on the far right. Doing so opens the :guilabel:`Open: Stock
move` pop-up window that displays how the reserved items were picked according to the removal
strategy.

In the :guilabel:`Open: Stock move` window, the :guilabel:`Pick from` field details where the
quantities to fulfill the :guilabel:`Demand` are picked. Since the order demanded eighty kilograms,
which exceeds the quantity in the opened package of `54 kg`, an unopened package of `100 kg` is
selected.

.. image:: least_packages/least-package.png
   :align: center
   :alt: Show which package was picked in the *Pick From* field.
