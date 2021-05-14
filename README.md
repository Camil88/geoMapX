Abstract: Application is a tool which serves to visualize coordinates on a map and perform spatial analysis. You can easily toggle between coordinates of deliveries or pickups, select areas on a map and more. The app is based on logistitcs industry.

Full Description: Application can be used in every industry branch where geolocation and GPS tracking play important role in daily operations. Application allows you to perform spatial analysis on a map. Moreover, dashboard with detailed data/charts and statistics is available for end users use.

In case of this app all the logic is based on logistics industry. Every single driver has a dedicated mobile app (different that this one, provided to drivers by logistics company) which only serves as a mean to set a shipments' status both on delivery or on pickup at customer's premises. For instance - driver goes to customer to pick up a shipment, opens his app and sets status 'delivered' (or different). Once he did it the coordinates of the place where status was set go directly to the database with some other information. Then I can visualize shipment's status coordinates on a map. App shows coordinates of such deliveries and pickups. You can toggle between them using blue buttons on the left- bottom side of the page (Pickup/Delivery/App - the last one shows driver's status coordinates). Need to mention that data loaded to the app consider just one day (2020-11-18). The reason for this is that it takes quite a long time for points to render on a map when date range is greater than 1 day. Moreover, app is dedicated to daily work with live data. Then it works fast. When it comes to older data user can download report. Below you can find a few crucial assumptions of the app which will make working on it better for the end user:

- once you open the app many lines connecting points are visible. Those lines connect coordinates of the status set for shipment by driver and coordinates of customer's business premises (on delivery/pickup). Why those lines are shorter or longer results from the fact that driver could set status somewhere else (not at customer's), not caring much about good quality he is obliged to. In this case, it's just enough to open this app to analyze which lines are the longest and probably which drivers potentially have a bad quality of work (status set far away from client = bad quality). You can then focus on those drivers and undertake steps to improve their quality on the business side. This fact causes, that when you toggle buttons (delivery/pickup) you will almost always see lines connecting driver's app and customers's coordinates. Buttons' logic (displaying) is also based on this assumption.

- sidebar panel allows you navigate to different areas of interest. Tab 'Transits' and 'Drivers' display tables with all transit numbers assigned to drivers. Each transit can consist of many orders (shipments) which driver must deliver or pickup. If you expand transit/driver row (in a table) you can see orders assigned to them. In every single row (tab 'Transits') there's also coloured 'P' or 'D' character which stands for Pickup/Delivery. In 'Drivers' tab you can see additional info about distance (in km) from place where driver set status to customer's coordinates. The bigger distance the worse (distance > 1km is highlighted in red). You can click whichever table's row and visualize (pulse icon) this shipment on a map (or all assigned to transit/driver).

- also in sidebar you can visit tab 'Report' which allows you generate Excel report for all shipments in given date range. 'Calendar' allows you pick up date range. On the top of a sidebar you can see 'Refresh' button which refreshes data and map (in this app it's not possible because it sctrictly connected with SQL server operations). Tab 'dashboard' will display dashboard with many useful utilities. It lets you have a closer look at data in details (table) and also have a broader view on how your division and drivers perform.

- on the bottom of the sidebar a small, blue button can be visible. By clicking on it, the panel consisting of 3 buttons fade in on the top of the page. First one is used to draw area on a map and select points as to analyze them quickly. When points are selected then controlbar on the right toggles and you can see quick stats summarizng selected points (chart + table). Second button allows you put choropleth on the map. It's worth adding that when shapes/area are selected then also tables in 'Transits' and 'Drivers' are filtered instantly which helps anlayze concrete drivers/transits/orders. Same logic here - by clicking any shape a controlbar on a right slides up showing some statistics. Third button - 'Heatmap' serves to display intensity of setting statuses by drivers in every region of the country.

- in header section you can see notifications and messages. Notifications ('bell' icon) are strictly related to SQL logic and inform end user of a driver entering customer's GPS area. Such areas can be defined programatically on a map or on a server side. When driver enters such area (set status or use any other tracking device e.g. in his truck) then notifications comes. Next button - 'messages from drivers'. Every single driver has an opportunity to send a message from his dedicated app (e.g. driver got stuck in a traffic, will be late, something happened) to end users (freigh-forwarders) as to communicate that they got a problem. Then, every end user which utylizes this map can see such messages in dropdown menu.

- buttons on the right pane (search & map layers). You can search for any address on a map, also you can change map layer.

- as for statistics visible in tables/charts: drivers sometimes add status far away from customer, if driver sets status > 1km then it's considered bad quality. Same with setting status up to 30 mins. If driver exceeds this time then it's also considered bad quality. As for serial sets - sometimes happen that driver set status for many orders, even for different customers, in one place. E.g. driver delivered shipment to customer and instead set status only for one shipment he set for 15 shipments for different customers. The reason of such behaviour is that sometimes drivers are not willing to follow the rules they should obey or don't want to cooperate with logistics company. When select points on a map/click shape (choropleth) then summary of all of those metrics shows up in a controlbar that slides from the right side of the page.

