# web-project-g19-lastt
web project-last

# web-project-g19
FoodWorld

https://github.com/sapirxpike/web-project-g19-lastt.git

the managing around the webstie infront of the DB happens threw the supported classes


We decided to create new classes auth & dishes
-each of them are use for DAO (data acsess object)
-those classe are using the DBMANAGER and export the questions to the DB and return the rellevant information
-they are in models directory
-we use the MVC principle

we created suppourt classes in models directory where we created 
functions which we use in the app.py for each of the uses and aimes
in the project

----example for using dbmanager - suppurted classes-----
from utilities.db.db_manager import dbManager

class Dishes:
    @staticmethod
    def get_dishes():
        # Get all dishes from database
        return dbManager.fetch("SELECT * FROM dishes")

@app.route('/giftcard', methods=['GET'])
def get_dishes():
    if session.get('logged_in'):
            dishes = Dishes.get_dishes()
            return render_template('giftcard.html', dishes = dishes)
    else:
        return redirect("/login")



class 1: class Auth:
+ function login - check if the user exist
need to uploud - (email , password)


+ function logout - disconnect the user from the website( guest not allowed to watch the website apart of about us page)


+ function register - the purpose if for new user/new guest in the website if to rgister to our website and then he can wtahc the whole website
need to uploud - (email, password, first_name, last_name)



class 2: class Dishes:
+ function get_dishes - Get all dishes from database


+ function get_user_dishes -Get dishe for specific user
need to uploud - (email)

+ function update_user_dish - Update user dish order in database
need to uploud - (email, dish_id, status)

+ function create_user_dish - Save user dish order to database
need to uploud - (email, dish_id)

+ function delete_user_dish - Delete user dish order from database
need to uploud - (email, dish_id)
