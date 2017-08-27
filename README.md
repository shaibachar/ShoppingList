Description:
  This project will manage my shopping list and all the metadata related.  

Data structures: 
 
 Item – will be anything that we should get.
   Will have:
    Name – unique Item name
    Description – will contain additional information on the item
    Importance integer from 1-100 
    Purchase date     
    Purchase price
    Start using date  
    Estimated end date
    End using date
    Renewal – is this item should be renewed
    Dependency – to what other items does this item is dependent.
    Activities – what activities we should fill in order to have the item. 
    moneyForDay – divide days to end by price.
  
  Group – will group items.
    Will have:
    Name – unique Item name
    Description – will contain additional information on the item
    Importance integer from 1-100 
    Items – all items related to the group
    Group state can be:
      Complete – when all items where purchased and activities complete and have more than half time between start using date and estimated end date
      Partial – when all items where purchased and activities complete but one or more have less than half time between start using date and estimated end date. 
      Incomplete – when not all items where purchased or not all activities where complete. Has at least one item purchased.
      Empty – when none of the items where purchased. 
    Completion Due date – the date when all items should be acquired. 
    Active – if the group is in process of acquire or we stopped acquiring items. 
    Activities – what activities we should fill in order to construct the group out of items 

  Project – project will contain groups.
    Will have: 
      Summed time of groups Completion Due dates.     
  Users – user is responsible for items 
    Will have:
      Name
      Items 
  
  Activities - what activities items or groups should fill in order to have the item or group complete.
    Will have:
      Name
      Estimated duration 
      Location 

The Server side should let me:
    Register items and relate them to groups and projects 
    Create activities relate to items and to groups
    Relate users to items
    Have a estimated date for group of items 

The Client side should let me:
    Query for items , groups , activities  and projects 
    Generate reports for each entity 
    Update the status of each entity
