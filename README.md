def add_single_data(data):
    new_data = input("Enter data to add: ")
    data.append(new_data)
    print("Data added successfully!")

def add_multiple_data(data):
    num_entries = int(input("Enter the number of entries to add: "))
    for _ in range(num_entries):
        new_data = input("Enter data: ")
        data.append(new_data)
    print("Data added successfully!")

def display_data(data):
    if not data:
        print("No data to display.")
    else:
        print("Data:")
        for i, item in enumerate(data, 1):
            print(f"{i}. {item}")

def delete_data(data):
    if not data:
        print("No data to delete.")
    else:
        index = int(input("Enter the index of the data to delete: ")) - 1
        if 0 <= index < len(data):
            del data[index]
            print("Data deleted successfully!")
        else:
            print("Invalid index.")

def update_data(data):
    if not data:
        print("No data to update.")
    else:
        index = int(input("Enter the index of the data to update: ")) - 1
        if 0 <= index < len(data):
            new_data = input("Enter new data: ")
            data[index] = new_data
            print("Data updated successfully!")
        else:
            print("Invalid index.")

def reverse_data(data):
    data.reverse()
    print("Data reversed successfully!")

def main():
    data = []
    while True:
        print("\nChoose an action:")
        print("1. Add a single data entry")
        print("2. Add multiple data entries")
        print("3. Display data")
        print("4. Delete data")
        print("5. Update data")
        print("6. Reverse data")
        print("7. Exit")

        choice = input("Enter your choice: ")

        if choice == '1':
            add_single_data(data)
        elif choice == '2':
            add_multiple_data(data)
        elif choice == '3':
            display_data(data)
        elif choice == '4':
            delete_data(data)
        elif choice == '5':
            update_data(data)
        elif choice == '6':
            reverse_data(data)
        elif choice == '7':
            break
        else:
            print("Invalid choice. Please try again.")

if __name__ == "__main__":
    main()
