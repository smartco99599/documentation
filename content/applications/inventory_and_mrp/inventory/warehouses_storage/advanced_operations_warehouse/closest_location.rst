========================
Closest location removal
========================

For the *closest location* removal strategy, products are picked based on the alphanumeric order of
storage location titles. This strategy requires businesses to store products that are ordered most
often in locations closest to the output area. Then, these locations are named in alphanumeric order
with the closest locations starting with letters closest to the beginning of the alphabet.

The aim is to save the warehouse worker from taking a long journey to a farther shelf when the
product is also available at a closer location.

.. _inventory/removal/sequence:

To understand *location sequence* in the closest removal strategy, consider the following example.

.. example::
   A product is stored in the following locations: `Shelf A/Pallet`, `Shelf A/Rack 1` and `Shelf
   A/Rack 2`.

   .. image:: closest_location/locations.png
      :align: center
      :alt: Show a mockup of real storage location in a warehouse.

   The sublocation `Pallet` is on the ground level, so products stored here are easier to retrieve,
   compared to requiring a forklift to reach `Rack 1` and `Rack 2`. The storage locations were
   strategically named in alphabetic order based on ease of access.

.. important::
   To use this removal strategy, the :guilabel:`Storage Locations` and :guilabel:`Multi-Step Routes`
   settings **must** be enabled in :menuselection:`Inventory --> Configuration --> Settings`.

.. seealso::
   :ref:`Set up removal strategy <inventory/routes/strategies/set>`

Location names
--------------

To configure location names, begin by navigating to :menuselection:`Inventory --> Configuration -->
Locations`. Select an existing location or click :guilabel:`New` to create a new one, and then enter
the desired name in the :guilabel:`Location Name` field.

Once the locations are named in alphabetical order based on their proximity to the output or packing
location, set the removal strategy on the :ref:`parent location <inventory/location-hierarchy>`. To
do that, in the :guilabel:`Locations` list, select the parent location of the alphabetically named
storage locations.

Doing so opens the form for the parent location. In the :guilabel:`Removal Strategy` field, select
:guilabel:`Closest Location`.

.. example::
   In a warehouse, the storage location `WH/Stock/Shelf 1` is located closest to the packing area,
   where products retrieved from shelves are packed for shipment. The popular product, `iPhone
   charger` is stored in three locations, `WH/Stock/Shelf 1`, `WH/Stock/Shelf 2`, and
   `WH/Stock/Shelf 3`.

   To use closest location , set the removal strategy on the parent location, 'WH/Stock'.

Workflow
--------

To see how the closest location removal strategy works, consider the popular product, `iPhone
charger` that is stored in `WH/Stock/Shelf 1`, `WH/Stock/Shelf 2`, and `WH/Stock/Shelf 3`. There are
fifteen, five, and thirty units in stock at each respective location.

.. tip::
   To check the on-hand stock at each storage location, navigate to the product form and click the
   :guilabel:`On Hand` smart button.

   .. image:: closest_location/on-hand-stock.png
      :align: center
      :alt: Show on-hand stock at all locations.

Create a :ref:`delivery order <inventory/delivery/one-step>` for eighteen units of the `iPhone
charger`, either by navigating to the :menuselection:`Sales app` and creating a new quotation, or
from the delivery orders dashboard in :menuselection:`Inventory --> Operations --> Deliveries`.

On the delivery order, the :guilabel:`Quantity` field displays the amount automatically picked
according to the removal strategy. For more details about *where* the units were picked, select the
:guilabel:`⦙≣ (bulleted list)` icon on the far right. Doing so opens the :guilabel:`Open: Stock
move` pop-up window that displays how the reserved items were picked according to the removal
strategy.

In the :guilabel:`Open: Stock move` window, the :guilabel:`Pick from` field details where the
quantities to fulfill the :guilabel:`Demand` are picked. All fifteen of the units stored at the
closest location, `WH/Stock/Shelf 1` are picked first. The remaining three units are then selected
from the second closest location, `WH/Stock/Shelf 2`.

.. image:: closest_location/stock-move-window.png
   :align: center
   :alt: Display *Pick From* quantities for the order for iPhone chargers.
