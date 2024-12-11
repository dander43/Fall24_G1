# Fall24, GROUP ONE

  # Members of Group one:
     Dudly Andre
         
     Daylon Anderson

     Demario Jackson
     
     Danish Naeem Rao

  # Submissions
    Dudley Andre,  https://github.com/andredudley/CSCI4211AD (empty)
  
    Demario Jackson, https://github.com/demariojackson/CSCI4221
  
    Daylon Anderson, https://github.com/dander43/CSCI4221-Anderson
  
    Danish Naeem Rao, No link

  # Combined information

    # Dudly Andre

    # Demario Jackson
        hello, my name is demario jackson

        this is the second *paragraph *

        Section 2
          TBA. I dont have anything yet
        About me
        My name is Demario Jackson and I'm currently looking for an internship in the Computer Science field.
        
    # Daylon Anderson
     
        Welcome to my page!

        We are excited to have you!

        cfdsgsafsgdhsafdshgf
     
     # Danish Naeem Rao

Daylon Anderson (below is the code provide and improved by the vscode openai addon)
import java.util.ArrayList;
import java.util.HashMap;
import java.util.List;
import java.util.Map;
import java.util.Scanner;

class StudySession {
    private String date;
    private String time;
    private List<String> topics;
    private List<String> members;

    public StudySession(String date, String time, List<String> topics, List<String> members) {
        this.date = date;
        this.time = time;
        this.topics = new ArrayList<>(topics);
        this.members = new ArrayList<>(members);
    }

    @Override
    public String toString() {
        return date + " at " + time + " | Topics: " + String.join(", ", topics) + " | Members: " + String.join(", ", members);
    }
}

class StudyGroup {
    private String name;
    private List<StudySession> sessions;

    public StudyGroup(String name) {
        this.name = name;
        this.sessions = new ArrayList<>();
    }

    public void addSession(String date, String time, List<String> topics, List<String> members) {
        StudySession session = new StudySession(date, time, topics, members);
        sessions.add(session);
        System.out.println("Study session added for " + date + " at " + time + ".");
    }

    public void viewSessions() {
        if (sessions.isEmpty()) {
            System.out.println("No study sessions scheduled for " + name + ".");
        } else {
            System.out.println("Study Sessions for " + name + ":");
            for (StudySession session : sessions) {
                System.out.println(session);
            }
        }
    }

    @Override
    public String toString() {
        return "Study Group: " + name + " | " + sessions.size() + " sessions scheduled.";
    }
}

class StudyGroupOrganizer {
    private Map<String, StudyGroup> groups;

    public StudyGroupOrganizer() {
        groups = new HashMap<>();
    }

    public void createGroup(String name) {
        if (groups.containsKey(name)) {
            System.out.println("A study group with this name already exists.");
        } else {
            groups.put(name, new StudyGroup(name));
            System.out.println("Study group '" + name + "' created.");
        }
    }

    public void addSessionToGroup(String groupName, String date, String time, List<String> topics, List<String> members) {
        StudyGroup group = groups.get(groupName);
        if (group == null) {
            System.out.println("No study group named '" + groupName + "'.");
        } else {
            group.addSession(date, time, topics, members);
        }
    }

    public void viewGroupSessions(String groupName) {
        StudyGroup group = groups.get(groupName);
        if (group != null) {
            group.viewSessions();
        } else {
            System.out.println("No study group named '" + groupName + "'.");
        }
    }

    public void listGroups() {
        if (groups.isEmpty()) {
            System.out.println("No study groups available.");
        } else {
            for (StudyGroup group : groups.values()) {
                System.out.println(group);
            }
        }
    }
}

public class StudyGroupOrganizerApp {
    public static void main(String[] args) {
        StudyGroupOrganizer organizer = new StudyGroupOrganizer();
        Scanner scanner = new Scanner(System.in);

        // Create some groups and sessions for demonstration
        organizer.createGroup("Math Study Group");
        organizer.createGroup("Physics Study Group");

        List<String> mathTopics = List.of("Calculus", "Algebra");
        List<String> mathMembers = List.of("Alice", "Bob");
        organizer.addSessionToGroup("Math Study Group", "2024-11-01", "10:00 AM", mathTopics, mathMembers);

        List<String> physicsTopics = List.of("Quantum Mechanics", "Relativity");
        List<String> physicsMembers = List.of("Charlie", "David");
        organizer.addSessionToGroup("Physics Study Group", "2024-11-03", "2:00 PM", physicsTopics, physicsMembers);

        // Display all groups
        organizer.listGroups();

        // Display sessions for a specific group
        organizer.viewGroupSessions("Math Study Group");

        scanner.close();
    }
}

- Daylon Anderson

first output test: 
Study group 'Math Study Group' created.
Study group 'Physics Study Group' created.
Study session added for 2024-11-01 at 10:00 AM.
Study session added for 2024-11-03 at 2:00 PM.
Study Group: Math Study Group | 1 sessions scheduled.
Study Group: Physics Study Group | 1 sessions scheduled.
Study Sessions for Math Study Group:
2024-11-01 at 10:00 AM | Topics: Calculus, Algebra | Members: Alice, Bob

APi Key:
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 



