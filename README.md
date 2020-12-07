# Njangui

Logic: 
1. The admin create a djangui for month x to month y. 
2. a djangui has manu tours, and each user will be the recipient of a single tour determined by the admin or randomly.
3. a tour has many cotisations and a cotisation is specific for a user. for example the user kaffo cotise(pay) 300 for each period od a djangui.
4. one djangui has many users, many tours and one tour has many cotisations, a cotisation is specific to a single tour.

Tables(entities models) and fields: 

*user 
.first_name : string
.last_name : string
.email : : string(email)
.password : String
.phone_number : String
.address : String 
.isAdmin : boolean 
.password resset)
.email verification)

*djamgui: 
.djangui_mame : string
.starting date : Date
. ending date : Date
.users : [Users].amount: int 
.isActive: boolean (default: true) turms to false when the djangui end (maybe end date + 3 days?)
(timing: weekly ? 2 weeks? monthly? ...)

*tour
.djangui : Djangui 
.starting_date : Date
.due_date : Date
. recipient : User
.total_amount: int
. cotisations : [Cotisation] : array of cotisations

*Cotisation 
. cotisation_name : Sting
.tour : Tour
.user : user 
.amount : int 
.cotisation_date: Date

