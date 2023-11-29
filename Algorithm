#include<bits/stdc++.h>
using namespace std;
#define ll long long
const int MAX=1e9+7;

struct Task {
    string title;
    string dueDate;
    bool completed;

    Task(const string& t, const string& date)
        : title(t), dueDate(date), completed(false) {}
};

bool compareTasks(const Task& task1, const Task& task2) {
    return task1.dueDate < task2.dueDate;
}

class TaskScheduler {
private:
    vector<Task> tasks;

public:
    void addTask(const string& title, const string& dueDate) {
        tasks.emplace_back(title, dueDate);
        std::sort(tasks.begin(), tasks.end(), compareTasks);
    }

    void viewTasks() const {
        cout << "Task List:\n";
        for (const auto& task : tasks) {
            std::cout << "Title: " << task.title << "\n";
            std::cout << "Due Date: " << task.dueDate << "\n";
            std::cout << "Status: " << (task.completed ? "Completed" : "Not Completed") << "\n";
            std::cout << "------------------------\n";
        }
    }

    void markTaskAsCompleted(const string& title) {
        for (auto& task : tasks) {
            if (task.title == title) {
                task.completed = true;
                break;
            }
        }
    }
};

int main() {
    TaskScheduler scheduler;

    scheduler.addTask("Complete Project", "2023-12-01");
    scheduler.addTask("Study for Exam", "2023-11-25");
    scheduler.addTask("Buy Groceries", "2023-11-20");

    scheduler.viewTasks();


    scheduler.markTaskAsCompleted("Study for Exam");

    std::cout << "\nUpdated Task List:\n";
    scheduler.viewTasks();

    return 0;
}
