import tkinter as tk

tasks = []


def add_task(task):
    tasks.append(task)
    print("Task added successfully.")


def list_tasks():
    if not tasks:
        print("No tasks found.")
    else:
        print("Tasks:")
        for index, task in enumerate(tasks, start=1):
            print(f"{index}. {task}")



def complete_task(task_index):
    if 1 <= task_index <= len(tasks):
        completed_task = tasks.pop(task_index - 1)
        print(f"Completed task: {completed_task}")
    else:
        print("Invalid task index.")


def main():
    print("Welcome to the Todo List App!")

    while True:
        print("\nMenu:")
        print("1. Add task")
        print("2. List tasks")
        print("3. Complete task")
        print("0. Exit")

        choice = input("Enter your choice: ")

        if choice == "1":
            task = input("Enter task: ")
            add_task(task)
        elif choice == "2":
            list_tasks()
        elif choice == "3":
            task_index = int(input("Enter task index: "))
            complete_task(task_index)
        elif choice == "0":
            print("Goodbye!")
            break
        else:
            print("Invalid choice. Please try again.")

    if not tasks:
        print("There is no task.")


window = tk.Tk()
window.title("Todo List App")

# Create a listbox to display the tasks
task_listbox = tk.Listbox(window, width=50)
task_listbox.pack()


def add_task():
    task = task_entry.get()
    if task:
        task_listbox.insert(tk.END, task)
        task_entry.delete(0, tk.END)


def delete_task():
    selected_task = task_listbox.curselection()
    if selected_task:
        task_listbox.delete(selected_task)


# Create an entry field and buttons
task_entry = tk.Entry(window, width=40)
task_entry.pack()

add_button = tk.Button(window, text="Add Task", command=add_task)
add_button.pack()

delete_button = tk.Button(window, text="Delete Task", command=delete_task)
delete_button.pack()

# Run the Tkinter event loop
window.mainloop()

if __name__ == "__main__":
    main()