=============================
Managing product variant BoMs
=============================

In Odoo, one bill of material can be used for multiple variants of the same product. Having a
consolidated BoM for a product with variants saves time by preventing the need to manage multiple
BoMs. To activate variants, simply navigate to :menuselection:`Inventory --> Configuration --> Settings --> Variants`. For more information on configuring product variants, refer to this page. 

.. image:: product_variants/bom-variants1.png
   :align: center
   :alt: 

Once product variants are fully configured, components may be assigned to specific variants on the
bill of materials. Each component may be assigned to multiple variants. Components with no variant
specificed are used in every variant of the product.

When defining BoMs for product variants by component assignment, the :guilabel:`Product Variant`
field in the main section of the BoM should be left blank, as shown below. This field is used only
when creating a BoM for one specific product variant.

.. image:: product_variants/kit-bom1.png
   :align: center

Note that the same principle applies for the configuration 
of operations.

.. image:: product_variants/kit-bom2.png
   :align: center

And for the production of by-products. 

.. image:: product_variants/kit-bom3.png
   :align: center
