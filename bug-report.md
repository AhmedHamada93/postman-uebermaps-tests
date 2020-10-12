## Summary:
    Map editor access and visitor access values are ignored.
## Description:
    When creating a map with certain editor and visitor access values, those values are ignored.
## Severity:
    High
## Priority:
    High
## Steps to Reproduce:
- API version: 2
- API Path: `https://uebermaps.com/api/v2/maps`
- Method: `POST`
- Request Body: 
    ````{
           "title": "{{MAP_TITLE}} {{timestamp}}",
           "description": "{{MAP_DESCRIPTION}} {{timestamp}}",
           "visibility": "{{MAP_VISIBILITY}}",
           "map_settings": {
               "editor_access": [
                   "can_create.map",
                   "can_administer.spots",
                   "can_administer.events",
                   "can_administer.comments",
                   "can_administer.attachments",
                   "can_administer.collaborators"
               ],
               "visitor_access": [
                   "can_administer.map",
                   "can_administer.spots",
                   "can_administer.events",
                   "can_administer.comments",
                   "can_administer.attachments",
                   "can_administer.collaborators"
               ],
               "respotting_to_this_map": true
           }
       }
  ````
## Expected Results
   Map created with sent editor and visitor access.
## Actual Results
   Map created with the following editor and visitor access.
 ````{ 
    "editor_access": [
        "can_none.map",
        "can_create.spots",
        "can_create.events",
        "can_create.comments",
        "can_create.attachments",
        "can_create.collaborators"
    ],
    "visitor_access": [
        "can_none.map",
        "can_none.spots",
        "can_none.events",
        "can_create.comments",
        "can_create.attachments",
        "can_none.collaborators"
    ]}
````
## Reported On
    09-15-2020 21:15 
