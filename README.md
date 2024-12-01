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


App Name: ScholarMate
1. Study Planner
Purpose: Help users organize and optimize their study schedules.
Key Features:

Customizable Schedule: Allow users to input study topics, durations, and deadlines.
Smart Recommendations: AI suggests study times based on available hours and priorities.
Progress Tracking: Visual charts to track study hours and completed tasks.
Reminders and Notifications: Gentle nudges for upcoming study sessions or deadlines.
Integration: Sync with calendar apps like Google Calendar or Apple Calendar.
2. AI-Powered Notes Summarizer
Purpose: Simplify large volumes of notes into concise summaries for quick review.
Key Features:

Text Import: Upload notes in multiple formats (PDF, Word, handwritten image-to-text OCR).
Summarization Modes:
Bullet Point Summary: For quick reviews.
Detailed Summary: For in-depth understanding.
Highlight Key Points: Automatically identify and mark essential information.
Searchable Summaries: Use keywords to find specific topics across notes.
Multilingual Support: Summarize notes in various languages.
3. Study Group Organizer
Purpose: Foster collaboration by helping users form and manage study groups.
Key Features:

Group Creation: Invite friends or connect with new people based on study topics.
Scheduling: AI suggests meeting times that work for all members.
Collaboration Tools:
Shared digital whiteboard.
Group note-taking space.
Real-time chat and video conferencing.
Progress Dashboard: Track group goals and milestones.
Privacy Settings: Manage group visibility and member permissions.
4. Mental Wellness Helper
Purpose: Ensure users maintain a healthy balance between studying and mental well-being.
Key Features:

Mindfulness Exercises: Guided meditations, breathing exercises, and quick stress relief practices.
Mood Tracker: Log daily emotions and identify stress patterns.
Break Reminders: Suggest optimal times for study breaks and relaxation.
Motivational Quotes: Periodically inspire users with uplifting messages.
Resource Library: Provide articles, podcasts, and videos on stress management and productivity.
Crisis Assistance: Links to mental health hotlines and support networks.
Technology Stack (For Development):
Frontend: React Native (cross-platform compatibility for iOS and Android).
Backend: Node.js and Firebase (real-time updates and scalable cloud backend).
AI Integration: OpenAI's API for summarization and recommendation systems.
Database: MongoDB (for flexible data storage).
Would you like a more detailed breakdown of any feature, or should we design the app interface next?



1. Home Screen
Purpose: Central hub for navigation and user overview.
Layout:
Header: Welcome message (e.g., "Welcome, [Name]!").
Quick Access Cards: Four main features displayed as interactive cards:
Study Planner: Show today's tasks and a progress bar.
Notes Summarizer: "Summarize Notes" quick action.
Study Groups: Highlight upcoming group events.
Mental Wellness Helper: Show the mood tracker or a motivational tip.
Navigation Bar (Bottom): Icons for Home, Planner, Groups, and Profile.
2. Study Planner Screen
Header: "Your Study Plan."
Layout:
Weekly Calendar View: Interactive schedule grid.
Task List: Below the calendar, list tasks for the selected day.
Each task includes: Title, duration, status (in progress, completed).
Floating Action Button (FAB): To add a new task.
Extras:
Filters: By subject or priority.
Progress Bar: Show weekly study completion percentage.
3. AI Notes Summarizer Screen
Header: "Summarize Your Notes."
Layout:
Upload Section: Drag-and-drop area for files or capture handwritten notes with the camera.
Summary Display:
Tabs for Bullet Points, Detailed Summary, and Keywords.
Export Button: Save summarized notes as PDF or text.
Search Bar: Search keywords within uploaded notes.
FAB: Access recently summarized notes.
4. Study Group Organizer Screen
Header: "Your Study Groups."
Layout:
Group Cards: Display existing groups with details:
Group name, subject, next meeting time, and number of members.
Create Group Button: Initiates a group creation flow.
Tabs:
All Groups: View all groups.
My Groups: Focus on user-led groups.
Group Interaction Page: Clicking a group card leads to a detailed page:
Chat interface.
Shared notes and meeting schedule.
5. Mental Wellness Helper Screen
Header: "Your Wellness Center."
Layout:
Mood Tracker Widget: Slider or emoji-based tracker (e.g., 😊, 😐, 😔).
Wellness Cards:
"Mindfulness Session," "Breathing Exercise," or "Motivational Quote."
Daily Tips Section: Rotating cards with quick advice.
Resource Button: Leads to articles and hotlines.


javasripct code provided below:
import React from 'react';
import { View, Text, StyleSheet, TouchableOpacity } from 'react-native';
import { NavigationContainer } from '@react-navigation/native';
import { createBottomTabNavigator } from '@react-navigation/bottom-tabs';
import Ionicons from 'react-native-vector-icons/Ionicons';

// Create the Tab Navigator
const Tab = createBottomTabNavigator();

// Home Screen
function HomeScreen() {
  return (
    <View style={styles.container}>
      <Text style={styles.title}>Welcome to ScholarMate!</Text>
      <TouchableOpacity style={styles.card}>
        <Text style={styles.cardText}>📅 Study Planner</Text>
      </TouchableOpacity>
      <TouchableOpacity style={styles.card}>
        <Text style={styles.cardText}>📝 Notes Summarizer</Text>
      </TouchableOpacity>
      <TouchableOpacity style={styles.card}>
        <Text style={styles.cardText}>👥 Study Groups</Text>
      </TouchableOpacity>
      <TouchableOpacity style={styles.card}>
        <Text style={styles.cardText}>❤️ Mental Wellness</Text>
      </TouchableOpacity>
    </View>
  );
}

// Study Planner Screen
function StudyPlannerScreen() {
  return (
    <View style={styles.container}>
      <Text style={styles.title}>Study Planner</Text>
      <Text style={styles.text}>Here’s where your tasks will appear!</Text>
    </View>
  );
}

// Notes Summarizer Screen
function NotesSummarizerScreen() {
  return (
    <View style={styles.container}>
      <Text style={styles.title}>Notes Summarizer</Text>
      <Text style={styles.text}>Upload notes to get started.</Text>
    </View>
  );
}

// Study Groups Screen
function StudyGroupsScreen() {
  return (
    <View style={styles.container}>
      <Text style={styles.title}>Study Groups</Text>
      <Text style={styles.text}>Join or create study groups here!</Text>
    </View>
  );
}

// Mental Wellness Helper Screen
function MentalWellnessScreen() {
  return (
    <View style={styles.container}>
      <Text style={styles.title}>Mental Wellness</Text>
      <Text style={styles.text}>Take a deep breath. You’ve got this!</Text>
    </View>
  );
}

// Main App Navigation
export default function App() {
  return (
    <NavigationContainer>
      <Tab.Navigator
        screenOptions={({ route }) => ({
          tabBarIcon: ({ focused, color, size }) => {
            const icons = {
              Home: 'home',
              Planner: 'calendar',
              Notes: 'document-text',
              Groups: 'people',
              Wellness: 'heart',
            };
            return <Ionicons name={icons[route.name]} size={size} color={color} />;
          },
          tabBarActiveTintColor: '#2e8b57',
          tabBarInactiveTintColor: 'gray',
        })}
      >
        <Tab.Screen name="Home" component={HomeScreen} />
        <Tab.Screen name="Planner" component={StudyPlannerScreen} />
        <Tab.Screen name="Notes" component={NotesSummarizerScreen} />
        <Tab.Screen name="Groups" component={StudyGroupsScreen} />
        <Tab.Screen name="Wellness" component={MentalWellnessScreen} />
      </Tab.Navigator>
    </NavigationContainer>
  );
}

// Shared Styles
const styles = StyleSheet.create({
  container: {
    flex: 1,
    justifyContent: 'center',
    alignItems: 'center',
    backgroundColor: '#f9f9f9',
  },
  title: {
    fontSize: 24,
    fontWeight: 'bold',
    marginBottom: 20,
  },
  text: {
    fontSize: 16,
    color: '#555',
    textAlign: 'center',
    marginHorizontal: 20,
  },
  card: {
    padding: 20,
    margin: 10,
    backgroundColor: '#e0f7fa',
    borderRadius: 10,
    width: '80%',
    alignItems: 'center',
  },
  cardText: {
    fontSize: 18,
    textAlign: 'center',
  },
});


(need AI APi) - Daylon Anderson
