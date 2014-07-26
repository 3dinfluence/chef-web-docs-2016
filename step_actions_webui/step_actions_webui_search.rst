.. This is an included how-to. 


Actions can be searched by action log name. Use filters for entity name, entity type, action type, remote request identifier, and tag. Most filter fields auto-complete from a list of possible values. Use wildcard searches and data ranges to fine-tune search results.

To search actions:

#. Open |webui_analytics|.
#. Choose a filter. (Most filter fields will auto-complete with a list of possible values.)

   Use ``Action Type`` to filter for the type of action, such as create, update, or delete.
   
   Use ``Entity Name`` to filter by |chef server| object name, such as cookbook, data bag, or role.
   
   Use ``Entity Type`` to filter by |chef server| object type, such as client, cookbook version, or role.
   
   Use ``Remote Request ID`` to filter by |chef client| run identifier that is reported back to |chef analytics| by |reporting|. This filter is useful for correlating actions that have occurred during specific |chef client| runs.
   
   Use ``Tags`` to filter by user-defined tags. Each user agent that performs an action---|knife|, |berkshelf|, |chef client|, |chef manage|---is assigned a tag.

   .. image:: ../../images/step_actions_webui_search_filters.png

#. Choose a date range. There are three options: after the specified date, before the specified date, or within a specified date range.

