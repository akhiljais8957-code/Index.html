<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>VillageSync - Smart Village Management System</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        :root {

            
            --primary: #8623c4;
            --secondary: #29ea80;
            --accent: #deef63;
            --light: #ecf0f1;
            --dark: #2c3e50;
        }
        
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background-color: #f5f7fa;
        }
        
        .gradient-bg {
            background: linear-gradient(135deg, #2c3e50 0%, #3498db 100%);
        }
        
        .card-shadow {
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
        }
        
        .feature-icon {
            width: 60px;
            height: 60px;
            border-radius: 50%;
            background-color: rgba(255, 255, 255, 0.1);
            display: flex;
            align-items: center;
            justify-content: center;
            margin-bottom: 1rem;
        }
        
        .dashboard-card {
            transition: all 0.3s ease;
        }
        
        .dashboard-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.1);
        }
        
        footer {
            background: linear-gradient(135deg, #2c3e50 0%, #1a2b3c 100%);
        }
        
        .event-calendar {
            border-radius: 10px;
            overflow: hidden;
        }
        
        .event-calendar .fc-header-toolbar {
            padding: 1rem;
            margin-bottom: 0;
        }
        
        .complaint-status-pending {
            background-color: #fff3cd;
            color: #856404;
        }
        
        .complaint-status-resolved {
            background-color: #d4edda;
            color: #155724;
        }
        
        .complaint-status-in-progress {
            background-color: #cce5ff;
            color: #004085;
        }
    </style>
    <link href="https://cdn.jsdelivr.net/npm/fullcalendar@5.11.3/main.min.css" rel="stylesheet">
</head>
<body>
    <!-- Navigation -->
    <nav class="gradient-bg text-white shadow-lg">
        <div class="container mx-auto px-4 py-3 flex justify-between items-center">
            <div class="flex items-center">
                <img src= "https://images.pexels.com/photos/280221/pexels-photo-280221.jpeg?cs=srgb&dl=pexels-pixabay-280221.jpg&fm=jpg" alt="Village Image"width="80"height="50" class="mr-3">
                <a href="#" class="text-xl font-bold">Welcome To My Village</a>
            </div>
            <div class="hidden md:flex space-x-6">
                <a href="#" class="hover:text-gray-200">Home</a>
                <a href="#features" class="hover:text-gray-200">Features</a>
                <a href="#services" class="hover:text-gray-200">Services</a>
                <a href="#contact" class="hover:text-gray-200">Contact</a>
            </div>
            <div class="md:hidden">
                <button class="mobile-menu-button p-2 focus:outline-none">
                    <i class="fas fa-bars text-xl"></i>
                </button>
            </div>
        </div>
        
        <!-- Mobile Menu -->
        <div class="mobile-menu hidden md:hidden bg-gray-800 px-4 pb-4">
            <a href="#" class="block py-2 hover:text-gray-200">Home</a>
            <a href="#features" class="block py-2 hover:text-gray-200">Features</a>
            <a href="#services" class="block py-2 hover:text-gray-200">Services</a>
            <a href="#contact" class="block py-2 hover:text-gray-200">Contact</a>
            <a href="login.html" class="block py-2 hover:text-gray-200">Login</a>
        </div>
    </nav>

    <!-- Hero Section -->
    <section class="gradient-bg text-white py-16 md:py-24">
        <div class="container mx-auto px-4 flex flex-col md:flex-row items-center">
            <div class="md:w-1/2 mb-8 md:mb-0">
                <h1 class="text-4xl md:text-5xl font-bold mb-4">Empowering Village Communities</h1>
                <p class="text-xl mb-6">A comprehensive digital platform for modern village administration, citizen engagement, and sustainable development.</p>
                <div class="flex flex-col sm:flex-row space-y-3 sm:space-y-0 sm:space-x-4">
                    <a href="register.html" class="bg-white text-gray-800 font-semibold px-6 py-3 rounded-lg hover:bg-gray-100 transition duration-300 text-center">Register Now</a>
                    <a href="#demo" class="border-2 border-white text-white font-semibold px-6 py-3 rounded-lg hover:bg-white hover:text-gray-800 transition duration-300 text-center">Watch Demo</a>
                </div>
            </div>
            <div class="md:w-1/2">
                <img src="https://cdn.pixabay.com/photo/2023/01/07/11/00/village-7702981_1280.jpg" alt=" Village Image"width="600"height="400" class="rounded-lg shadow-2xl">
            </div>
        </div>
    </section>

    <!-- Announcements Section -->
    <section class="bg-white py-12">
        <div class="container mx-auto px-4">
            <h2 class="text-3xl font-bold text-center mb-12 text-gray-800">Latest Announcements</h2>
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6">
                <div class="bg-gray-50 rounded-lg p-6 border border-gray-200 card-shadow">
                    <div class="flex items-center mb-3">
                        <span class="bg-blue-100 text-blue-800 text-xs font-semibold px-2.5 py-0.5 rounded mr-3">Important</span>
                        <span class="text-gray-500 text-sm">July 15, 2023</span>
                    </div>
                    <h3 class="text-xl font-semibold mb-2">Water Supply Maintenance</h3>
                    <p class="text-gray-600 mb-4">Water supply will be temporarily suspended on July 18th for maintenance work from 9 AM to 5 PM.</p>
                    <button class="text-blue-600 font-medium hover:text-blue-800">Read More →</button>
                </div>
                
                <div class="bg-gray-50 rounded-lg p-6 border border-gray-200 card-shadow">
                    <div class="flex items-center mb-3">
                        <span class="bg-green-100 text-green-800 text-xs font-semibold px-2.5 py-0.5 rounded mr-3">Event</span>
                        <span class="text-gray-500 text-sm">July 10, 2023</span>
                    </div>
                    <h3 class="text-xl font-semibold mb-2">Village Health Camp</h3>
                    <p class="text-gray-600 mb-4">Free health checkup camp will be organized at the community center on July 22nd from 10 AM to 4 PM.</p>
                    <button class="text-blue-600 font-medium hover:text-blue-800">Read More →</button>
                </div>
                
                <div class="bg-gray-50 rounded-lg p-6 border border-gray-200 card-shadow">
                    <div class="flex items-center mb-3">
                        <span class="bg-red-100 text-red-800 text-xs font-semibold px-2.5 py-0.5 rounded mr-3">Alert</span>
                        <span class="text-gray-500 text-sm">July 5, 2023</span>
                    </div>
                    <h3 class="text-xl font-semibold mb-2">Garbage Collection Schedule Change</h3>
                    <p class="text-gray-600 mb-4">From next week, garbage collection days will change to Monday, Wednesday, and Friday.</p>
                    <button class="text-blue-600 font-medium hover:text-blue-800">Read More →</button>
                </div>
            </div>
            <div class="text-center mt-8">
                <a href="announcements.html" class="inline-block bg-gray-800 text-white px-6 py-2 rounded-lg hover:bg-gray-700 transition duration-300">View All Announcements</a>
            </div>
        </div>
    </section>

    <!-- Features Section -->
    <section id="features" class="py-16 bg-gray-50">
        <div class="container mx-auto px-4">
            <h2 class="text-3xl font-bold text-center mb-12 text-gray-800">Key Features</h2>
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
                <div class="p-6 rounded-lg card-shadow dashboard-card bg-white">
                    <div class="feature-icon mx-auto">
                        <i class="fas fa-bell text-2xl text-blue-600"></i>
                    </div>
                    <h3 class="text-xl font-semibold mb-3 text-center">Announcements</h3>
                    <p class="text-gray-600 text-center">Instant notifications for important village news, events, and emergency alerts delivered directly to residents.</p>
                </div>
                
                <div class="p-6 rounded-lg card-shadow dashboard-card bg-white">
                    <div class="feature-icon mx-auto">
                        <i class="fas fa-comments text-2xl text-green-600"></i>
                    </div>
                    <h3 class="text-xl font-semibold mb-3 text-center">Complaint Management</h3>
                    <p class="text-gray-600 text-center">Streamlined system for residents to report issues with real-time tracking of complaint resolution status.</p>
                </div>
                
                <div class="p-6 rounded-lg card-shadow dashboard-card bg-white">
                    <div class="feature-icon mx-auto">
                        <i class="fas fa-calendar-alt text-2xl text-purple-600"></i>
                    </div>
                    <h3 class="text-xl font-semibold mb-3 text-center">Event Calendar</h3>
                    <p class="text-gray-600 text-center">Centralized calendar for village events, meetings, and cultural programs with RSVP functionality.</p>
                </div>
                
                <div class="p-6 rounded-lg card-shadow dashboard-card bg-white">
                    <div class="feature-icon mx-auto">
                        <i class="fas fa-users text-2xl text-orange-600"></i>
                    </div>
                    <h3 class="text-xl font-semibold mb-3 text-center">Resident Directory</h3>
                    <p class="text-gray-600 text-center">Secure directory of residents with customizable privacy settings for better community networking.</p>
                </div>
                
                <div class="p-6 rounded-lg card-shadow dashboard-card bg-white">
                    <div class="feature-icon mx-auto">
                        <i class="fas fa-rupee-sign text-2xl text-red-600"></i>
                    </div>
                    <h3 class="text-xl font-semibold mb-3 text-center">Financial Transparency</h3>
                    <p class="text-gray-600 text-center">Public dashboard for village funds, expenditures, and budget allocation with downloadable reports.</p>
                </div>
                
                <div class="p-6 rounded-lg card-shadow dashboard-card bg-white">
                    <div class="feature-icon mx-auto">
                        <i class="fas fa-chart-line text-2xl text-teal-600"></i>
                    </div>
                    <h3 class="text-xl font-semibold mb-3 text-center">Resource Management</h3>
                    <p class="text-gray-600 text-center">Track and optimize allocation of village resources like community facilities, equipment, and supplies.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Dashboard Preview -->
    <section class="py-16 bg-white">
        <div class="container mx-auto px-4">
            <h2 class="text-3xl font-bold text-center mb-12 text-gray-800">Administrator Dashboard</h2>
            <div class="bg-gray-50 border border-gray-200 rounded-lg p-6 card-shadow">
                <div class="grid grid-cols-1 lg:grid-cols-3 gap-6 mb-6">
                    <div class="bg-white p-4 rounded-lg border border-gray-200">
                        <h3 class="font-semibold text-lg mb-2">Complaints Summary</h3>
                        <div class="space-y-3">
                            <div class="flex justify-between items-center">
                                <span>Total Complaints</span>
                                <span class="font-bold">142</span>
                            </div>
                            <div class="flex justify-between items-center">
                                <span>Resolved</span>
                                <span class="font-bold text-green-600">98 (69%)</span>
                            </div>
                            <div class="flex justify-between items-center">
                                <span>In Progress</span>
                                <span class="font-bold text-blue-600">32 (23%)</span>
                            </div>
                            <div class="flex justify-between items-center">
                                <span>Pending</span>
                                <span class="font-bold text-yellow-600">12 (8%)</span>
                            </div>
                        </div>
                    </div>
                    
                    <div class="bg-white p-4 rounded-lg border border-gray-200">
                        <h3 class="font-semibold text-lg mb-2">Recent Events</h3>
                        <div class="space-y-3">
                            <div class="flex items-start">
                                <div class="bg-blue-100 text-blue-800 rounded-full w-8 h-8 flex items-center justify-center mr-3 flex-shrink-0">
                                    <i class="fas fa-calendar-alt"></i>
                                </div>
                                <div>
                                    <p class="font-medium">Village Cleanup Drive</p>
                                    <p class="text-sm text-gray-500">Tomorrow, 8 AM - Community Center</p>
                                </div>
                            </div>
                            <div class="flex items-start">
                                <div class="bg-green-100 text-green-800 rounded-full w-8 h-8 flex items-center justify-center mr-3 flex-shrink-0">
                                    <i class="fas fa-users"></i>
                                </div>
                                <div>
                                    <p class="font-medium">Gram Sabha Meeting</p>
                                    <p class="text-sm text-gray-500">July 25th, 4 PM - Panchayat Office</p>
                                </div>
                            </div>
                        </div>
                    </div>
                    
                    <div class="bg-white p-4 rounded-lg border border-gray-200">
                        <h3 class="font-semibold text-lg mb-2">Quick Actions</h3>
                        <div class="grid grid-cols-2 gap-3">
                            <button class="bg-blue-100 text-blue-800 p-2 rounded-lg hover:bg-blue-200 transition flex flex-col items-center">
                                <i class="fas fa-bullhorn mb-1"></i>
                                <span class="text-sm">New Announcement</span>
                            </button>
                            <button class="bg-green-100 text-green-800 p-2 rounded-lg hover:bg-green-200 transition flex flex-col items-center">
                                <i class="fas fa-calendar-plus mb-1"></i>
                                <span class="text-sm">Add Event</span>
                            </button>
                            <button class="bg-purple-100 text-purple-800 p-2 rounded-lg hover:bg-purple-200 transition flex flex-col items-center">
                                <i class="fas fa-chart-pie mb-1"></i>
                                <span class="text-sm">Generate Report</span>
                            </button>
                            <button class="bg-orange-100 text-orange-800 p-2 rounded-lg hover:bg-orange-200 transition flex flex-col items-center">
                                <i class="fas fa-user-plus mb-1"></i>
                                <span class="text-sm">Add Resident</span>
                            </button>
                        </div>
                    </div>
                </div>
                
                <!-- Complaints Table -->
                <div class="bg-white p-4 rounded-lg border border-gray-200 mb-6">
                    <h3 class="font-semibold text-lg mb-3">Recent Complaints</h3>
                    <div class="overflow-x-auto">
                        <table class="min-w-full divide-y divide-gray-200">
                            <thead class="bg-gray-50">
                                <tr>
                                    <th class="px-6 py-3 text-left text-xs font-medium text-gray-500 uppercase tracking-wider">ID</th>
                                    <th class="px-6 py-3 text-left text-xs font-medium text-gray-500 uppercase tracking-wider">Category</th>
                                    <th class="px-6 py-3 text-left text-xs font-medium text-gray-500 uppercase tracking-wider">Description</th>
                                    <th class="px-6 py-3 text-left text-xs font-medium text-gray-500 uppercase tracking-wider">Resident</th>
                                    <th class="px-6 py-3 text-left text-xs font-medium text-gray-500 uppercase tracking-wider">Date</th>
                                    <th class="px-6 py-3 text-left text-xs font-medium text-gray-500 uppercase tracking-wider">Status</th>
                                </tr>
                            </thead>
                            <tbody class="bg-white divide-y divide-gray-200">
                                <tr>
                                    <td class="px-6 py-4 whitespace-nowrap text-sm font-medium text-gray-900">#137</td>
                                    <td class="px-6 py-4 whitespace-nowrap text-sm text-gray-500">Sanitation</td>
                                    <td class="px-6 py-4 text-sm text-gray-500">Garbage not collected from street</td>
                                    <td class="px-6 py-4 whitespace-nowrap text-sm text-gray-500">Ramesh Patel</td>
                                    <td class="px-6 py-4 whitespace-nowrap text-sm text-gray-500">Jul 14, 2023</td>
                                    <td class="px-6 py-4 whitespace-nowrap">
                                        <span class="px-2 py-1 text-xs rounded-full complaint-status-resolved">Resolved</span>
                                    </td>
                                </tr>
                                <tr>
                                    <td class="px-6 py-4 whitespace-nowrap text-sm font-medium text-gray-900">#138</td>
                                    <td class="px-6 py-4 whitespace-nowrap text-sm text-gray-500">Road</td>
                                    <td class="px-6 py-4 text-sm text-gray-500">Pothole near market area</td>
                                    <td class="px-6 py-4 whitespace-nowrap text-sm text-gray-500">Suman Mehta</td>
                                    <td class="px-6 py-4 whitespace-nowrap text-sm text-gray-500">Jul 13, 2023</td>
                                    <td class="px-6 py-4 whitespace-nowrap">
                                        <span class="px-2 py-1 text-xs rounded-full complaint-status-in-progress">In Progress</span>
                                    </td>
                                </tr>
                                <tr>
                                    <td class="px-6 py-4 whitespace-nowrap text-sm font-medium text-gray-900">#139</td>
                                    <td class="px-6 py-4 whitespace-nowrap text-sm text-gray-500">Water Supply</td>
                                    <td class="px-6 py-4 text-sm text-gray-500">Low water pressure</td>
                                    <td class="px-6 py-4 whitespace-nowrap text-sm text-gray-500">Vijay Singh</td>
                                    <td class="px-6 py-4 whitespace-nowrap text-sm text-gray-500">Jul 12, 2023</td>
                                    <td class="px-6 py-4 whitespace-nowrap">
                                        <span class="px-2 py-1 text-xs rounded-full complaint-status-pending">Pending</span>
                                    </td>
                                </tr>
                            </tbody>
                        </table>
                    </div>
                </div>
                
                <!-- Calendar -->
                <div class="bg-white p-4 rounded-lg border border-gray-200">
                    <h3 class="font-semibold text-lg mb-3">Village Calendar</h3>
                    <div id="calendar" class="event-calendar"></div>
                </div>
            </div>
        </div>
    </section>

    <!-- Services Section -->
    <section id="services" class="py-16 bg-gray-50">
        <div class="container mx-auto px-4">
            <h2 class="text-3xl font-bold text-center mb42 text-gray-800">Our Services</h2>
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
                <div class="p-6 rounded-lg card-shadow dashboard-card bg-white">
                    <img src="https://placehold.co/600x400/2c3e50/FFFFFF?text=Resident+Portal" alt="Digital portal interface showing resident profile, services and village information" class="w-full h-48 object-cover rounded-t-lg mb-4">
                    <h3 class="text-xl font-semibold mb-2">Resident Portal</h3>
                    <p class="text-gray-600 mb-4">Personalized dashboard for residents to access services, pay bills, and view announcements.</p>
                    <a href="#" class="text-blue-600 font-medium hover:text-blue-800">Learn More →</a>
                </div>
                
                <div class="p-6 rounded-lg card-shadow dashboard-card bg-white">
                    <img src="https://placehold.co/600x400/2c3e50/FFFFFF?text=Administration+Dashboard" alt="Administrative interface showing village statistics and management tools" class="w-full h-48 object-cover rounded-t-lg mb-4">
                    <h3 class="text-xl font-semibold mb-2">Administration Dashboard</h3>
                    <p class="text-gray-600 mb-4">Comprehensive tools for village officials to manage operations, resources, and community engagement.</p>
                    <a href="#" class="text-blue-600 font-medium hover:text-blue-800">Learn More →</a>
                </div>
                
                <div class="p-6 rounded-lg card-shadow dashboard-card bg-white">
                    <img src="https://placehold.co/600x400/2c3e50/FFFFFF?text=Mobile+App" alt="Smartphone showing the village management mobile application interface" class="w-full h-48 object-cover rounded-t-lg mb-4">
                    <h3 class="text-xl font-semibold mb-2">Mobile Application</h3>
                    <p class="text-gray-600 mb-4">Native mobile apps for iOS and Android to access village services on the go.</p>
                    <a href="#" class="text-blue-600 font-medium hover:text-blue-800">Learn More →</a>
                </div>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section id="contact" class="py-16 bg-white">
        <div class="container mx-auto px-4">
            <h2 class="text-3xl font-bold text-center mb-12 text-gray-800">Contact Us</h2>
            <div class="flex flex-col lg:flex-row gap-12">
                <div class="lg:w-1/2">
                    <div class="bg-gray-50 p-6 rounded-lg border border-gray-200 card-shadow">
                        <h3 class="text-xl font-semibold mb-4">Send us a message</h3>
                        <form>
                            <div class="mb-4">
                                <label for="name" class="block text-gray-700 font-medium mb-2">Name</label>
                                <input type="text" id="name" class="w-full px-4 py-2 border border-gray-300 rounded-lg focus:outline-none focus:ring-2 focus:ring-blue-500">
                            </div>
                            <div class="mb-4">
                                <label for="email" class="block text-gray-700 font-medium mb-2">Email</label>
                                <input type="email" id="email" class="w-full px-4 py-2 border border-gray-300 rounded-lg focus:outline-none focus:ring-2 focus:ring-blue-500">
                            </div>
                            <div class="mb-4">
                                <label for="subject" class="block text-gray-700 font-medium mb-2">Subject</label>
                                <input type="text" id="subject" class="w-full px-4 py-2 border border-gray-300 rounded-lg focus:outline-none focus:ring-2 focus:ring-blue-500">
                            </div>
                            <div class="mb-4">
                                <label for="message" class="block text-gray-700 font-medium mb-2">Message</label>
                                <textarea id="message" rows="5" class="w-full px-4 py-2 border border-gray-300 rounded-lg focus:outline-none focus:ring-2 focus:ring-blue-500"></textarea>
                            </div>
                            <button type="submit" class="w-full bg-blue-600 text-white py-2 px-4 rounded-lg hover:bg-blue-700 transition duration-300">Send Message</button>
                        </form>
                    </div>
                </div>
                <div class="lg:w-1/2">
                    <div class="bg-gray-50 p-6 rounded-lg border border-gray-200 card-shadow mb-6">
                        <h3 class="text-xl font-semibold mb-4">Visit Us</h3>
                        <div class="space-y-4">
                            <div>
                                <h4 class="font-medium text-gray-700">Village Panchayat Office</h4>
                                <p class="text-gray-600">Main Street, Village Center</p>
                                <p class="text-gray-600">District: Your District</p>
                                <p class="text-gray-600">State: Your State</p>
                                <p class="text-gray-600">PIN: 123456</p>
                            </div>
                            <div class="pt-4 border-t border-gray-200">
                                <h4 class="font-medium text-gray-700">Office Hours</h4>
                                <p class="text-gray-600">Monday to Friday: 9:00 AM - 5:00 PM</p>
                                <p class="text-gray-600">Saturday: 10:00 AM - 2:00 PM</p>
                                <p class="text-gray-600">Sunday: Closed</p>
                            </div>
                        </div>
                    </div>
                    <div class="bg-gray-50 p-6 rounded-lg border border-gray-200 card-shadow">
                        <h3 class="text-xl font-semibold mb-4">Quick Contacts</h3>
                        <div class="space-y-3">
                            <div class="flex items-start">
                                <div class="bg-green-100 text-green-800 rounded-full w-10 h-10 flex items-center justify-center mr-3 flex-shrink-0">
                                    <i class="fas fa-phone-alt"></i>
                                </div>
                                <div>
                                    <p class="font-medium text-gray-700">Gram Panchayat Office</p>
                                    <p class="text-gray-600">+91 XXXXXXXXXX</p>
                                </div>
                            </div>
                            <div class="flex items-start">
                                <div class="bg-blue-100 text-blue-800 rounded-full w-10 h-10 flex items-center justify-center mr-3 flex-shrink-0">
                                    <i class="fas fa-envelope"></i>
                                </div>
                                <div>
                                    <p class="font-medium text-gray-700">Email Support</p>
                                    <p class="text-gray-600">support@villagesync.org</p>
                                </div>
                            </div>
                            <div class="flex items-start">
                                <div class="bg-purple-100 text-purple-800 rounded-full w-10 h-10 flex items-center justify-center mr-3 flex-shrink-0">
                                    <i class="fas fa-exclamation-triangle"></i>
                                </div>
                                <div>
                                    <p class="font-medium text-gray-700">Emergency</p>
                                    <p class="text-gray-600">+91 XXXXXXXXXX</p>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="text-white py-12">
        <div class="container mx-auto px-4">
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-8">
                <div>
                    <h3 class="text-xl font-semibold mb-4">VillageSync</h3>
                    <p class="text-gray-300">Empowering village communities through digital transformation and smart governance solutions.</p>
                    <div class="flex space-x-4 mt-4">
                        <a href="#" class="text-gray-300 hover:text-white"><i class="fab fa-facebook-f"></i></a>
                        <a href="#" class="text-gray-300 hover:text-white"><i class="fab fa-twitter"></i></a>
                        <a href="#" class="text-gray-300 hover:text-white"><i class="fab fa-instagram"></i></a>
                        <a href="#" class="text-gray-300 hover:text-white"><i class="fab fa-linkedin-in"></i></a>
                    </div>
                </div>
                <div>
                    <h4 class="text-lg font-semibold mb-4">Quick Links</h4>
                    <ul class="space-y-2">
                        <li><a href="#" class="text-gray-300 hover:text-white">Home</a></li>
                        <li><a href="#" class="text-gray-300 hover:text-white">Features</a></li>
                        <li><a href="#" class="text-gray-300 hover:text-white">Services</a></li>
                        <li><a href="#" class="text-gray-300 hover:text-white">About Us</a></li>
                        <li><a href="#" class="text-gray-300 hover:text-white">Contact</a></li>
                    </ul>
                </div>
                <div>
                    <h4 class="text-lg font-semibold mb-4">Services</h4>
                    <ul class="space-y-2">
                        <li><a href="#" class="text-gray-300 hover:text-white">Resident Portal</a></li>
                        <li><a href="#" class="text-gray-300 hover:text-white">Administration</a></li>
                        <li><a href="#" class="text-gray-300 hover:text-white">Mobile App</a></li>
                        <li><a href="#" class="text-gray-300 hover:text-white">Training</a></li>
                        <li><a href="#" class="text-gray-300 hover:text-white">Support</a></li>
                    </ul>
                </div>
                <div>
                    <h4 class="text-lg font-semibold mb-4">Newsletter</h4>
                    <p class="text-gray-300 mb-4">Subscribe to our newsletter for the latest updates.</p>
                    <form class="flex">
                        <input type="email" placeholder="Your email" class="px-4 py-2 rounded-l-lg focus:outline-none text-gray-800 w-full">
                        <button type="submit" class="bg-blue-600 px-4 py-2 rounded-r-lg hover:bg-blue-700 transition duration-300">Subscribe</button>
                    </form>
                </div>
            </div>
            <div class="border-t border-gray-700 mt-12 pt-8 text-center text-gray-400">
                <p>© 2023 VillageSync. All rights reserved.</p>
            </div>
        </div>
    </footer>

    <script src="https://cdn.jsdelivr.net/npm/fullcalendar@5.11.3/main.min.js"></script>
    <script>
        // Mobile Menu Toggle
        document.querySelector('.mobile-menu-button').addEventListener('click', function() {
            document.querySelector('.mobile-menu').classList.toggle('hidden');
        });

        // Initialize Calendar
        document.addEventListener('DOMContentLoaded', function() {
            var calendarEl = document.getElementById('calendar');
            var calendar = new FullCalendar.Calendar(calendarEl, {
                initialView: 'dayGridMonth',
                headerToolbar: {
                    left: 'prev,next today',
                    center: 'title',
                    right: 'dayGridMonth,timeGridWeek,timeGridDay'
                },
                events: [
                    {
                        title: 'Gram Sabha Meeting',
                        start: '2023-07-20',
                        end: '2023-07-20',
                        className: 'bg-blue-500 border-none'
                    },
                    {
                        title: 'Village Cleanup',
                        start: '2023-07-22',
                        end: '2023-07-22',
                        className: 'bg-green-500 border-none'
                    },
                    {
                        title: 'Health Camp',
                        start: '2023-07-25',
                        end: '2023-07-26',
                        className: 'bg-purple-500 border-none'
                    }
                ],
                eventContent: function(arg) {
                    return {
                        html: `<div class="fc-event-main-frame">
                            <div class="fc-event-title">${arg.event.title}</div>
                        </div>`
                    };
                }
            });
            calendar.render();
        });

        // Smooth scrolling for anchor links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function(e) {
                e.preventDefault();
                document.querySelector(this.getAttribute('href')).scrollIntoView({
                    behavior: 'smooth'
                });
            });
        });
    </script>
</body>
</html>
