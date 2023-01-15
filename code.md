#to do list


user_input = 'random'
data = []

**#define a menu function to be called**


def show_menu():
    print('Menu: ')
    print('1. Add an item')
    print('2. Mark as done')
    print('3. View items')
    print('4. Exit')

while user_input != '4':
    show_menu()
    user_input = input('Enter your choice: ')

    if user_input == '1':
        item = input('What are you adding?')
        data.append(item)
        print('Added item:', item)

    elif user_input == '2':
        item = input('What is to be marked as done(removed)?: ')
        **#error check to make sure the item is in the list**
        if item in data:
            data.remove(item)
            print('Removed item:' item)
        else:
            print('Item does not exist in the list')    
    elif user_input == '3':
        print('list of to do items')
        for item in data:
            print(item)


    elif user_input == '4':
        print('goodbye')

    else: 
        print('please enter one of 1,2,3 or 4')



#note

#the ** are just to make the lines bold in the md file
