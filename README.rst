Introduction
=====================

pyzootool wraps the API of http://www.zootool.com. It's currently still very early in development, and not quite everything works.

What Works 
=====================

- Grabbing items by uid
- Grabbing items by popularity
- Grabbing items by username
- Getting information on a user
- Getting list of followers that a user has
- Getting list of friends that a user has

What Doesn't Work
=====================

- Authentication and anything that needs it
- Adding items to zootool.com

Examples
=====================

Here's a few examples of what you can do with this tool::

	from pyzootool import controller
	zoocontrol = controller.ZooControl(apikey=YOUR_API_KEY)
	
	## User information
	followers = zoocontrol.user.get_user_followers('username')
	friends = zoocontrol.user.get_user_friends('username')
	userinfo = zoocontrol.user.get_userinfo('username')
	
	## Items
	popular_items = zoocontrol.item.get_popular('week')
	user_items = zoocontrol.item.get_items_by_user('username')
	item = zoocontrol.item.get_item('uid')