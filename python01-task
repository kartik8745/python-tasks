class Contact:
    def __init__(self, name, phone, email, address):
        self.name = name
        self.phone = phone
        self.email = email
        self.address = address

class ContactBook:
    def __init__(self):
        self.contacts = {}

    def add_contact(self):
        name = input("Enter the name: ")
        phone = input("Enter the phone number: ")
        email = input("Enter the email: ")
        address = input("Enter the address: ")
        contact = Contact(name, phone, email, address)
        self.contacts[name] = contact
        print(f"Contact {name} added successfully!")

    def delete_contact(self):
        name = input("Enter the name of the contact to delete: ")
        if name in self.contacts:
            del self.contacts[name]
            print(f"Contact {name} deleted successfully!")
        else:
            print(f"Contact {name} not found!")

    def view_contacts(self):
        if not self.contacts:
            print("Contact book is empty!")
        else:
            print("Contact Book:")
            for contact in self.contacts.values():
                print(f"Name: {contact.name}, Phone: {contact.phone}, Email: {contact.email}, Address: {contact.address}")

    def search_contact(self):
        name = input("Enter the name to search: ")
        if name in self.contacts:
            contact = self.contacts[name]
            print(f"Contact {name} found!")
            print(f"Phone: {contact.phone}, Email: {contact.email}, Address: {contact.address}")
        else:
            print(f"Contact {name} not found!")
                    
    def update_contact(self):
        name = input("Enter the name of the contact to update: ")
        if name in self.contacts:
            contact = self.contacts[name]
            print("Enter new details (press enter to keep current value):")
            contact.name = input(f"Name ({contact.name}): ") or contact.name
            contact.phone = input(f"Phone ({contact.phone}): ") or contact.phone
            contact.email = input(f"Email ({contact.email}): ") or contact.email
            contact.address = input(f"Address ({contact.address}): ") or contact.address
            print(f"Contact {name} updated successfully!")
        else:
            print(f"Contact {name} not found!")

def main():
    contact_book = ContactBook()

    while True:
        print("\nContact Book Menu:")
        print("1. Add Contact")
        print("2. Delete Contact")
        print("3. View Contacts")
        print("4. Search Contact")
        print("5. Update Contact")
        print("6. Exit")

        choice = input("Enter your choice: ")

        if choice == "1":
            contact_book.add_contact()
        elif choice == "2":
            contact_book.delete_contact()
        elif choice == "3":
            contact_book.view_contacts()
        elif choice == "4":
            contact_book.search_contact()
        elif choice == "5":
            contact_book.update_contact()
        elif choice == "6":
            print("Thank you for using this !!")
            break
        else:
            print("Invalid choice. Please try again!")
            
if __name__ == "__main__":
    main()
