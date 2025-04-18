```javascript
import { Card, CardContent } from "@/components/ui/card";
import { Badge } from "@/components/ui/badge";
import { Button } from "@/components/ui/button";
import { Tabs, TabsContent, TabsList, TabsTrigger } from "@/components/ui/tabs";
import { ScrollArea } from "@/components/ui/scroll-area";
import { Switch } from "@/components/ui/switch";
import { Sun, Moon, Download } from "lucide-react";
import { motion } from "framer-motion";
import Image from "next/image";
import { useState } from "react";

export default function MehulJainProfile() {
  const [darkMode, setDarkMode] = useState(false);

  return (
    <div className={`p-4 md:p-8 space-y-6 min-h-screen transition-all duration-500 ${darkMode ? 'bg-black text-white' : 'bg-white text-black'}`}>
      <div className="flex justify-between items-center">
        <h1 className="text-3xl font-bold">👨‍💻 Mehul Jain</h1>
        <div className="flex items-center gap-4">
          <Switch checked={darkMode} onCheckedChange={() => setDarkMode(!darkMode)} />
          {darkMode ? <Moon size={20} /> : <Sun size={20} />}
          <Button variant="outline" size="sm" onClick={() => window.print()}>
            <Download className="mr-2 h-4 w-4" /> PDF
          </Button>
        </div>
      </div>

      <motion.div className="flex justify-center" initial={{ opacity: 0 }} animate={{ opacity: 1 }} transition={{ duration: 1 }}>
        <Image
          src="https://avatars.githubusercontent.com/u/130870177?v=4"
          alt="Mehul Jain Avatar"
          width={120}
          height={120}
          className="rounded-full border-4 border-blue-500"
        />
      </motion.div>

      <motion.p className="text-muted-foreground text-center" initial={{ opacity: 0 }} animate={{ opacity: 1 }} transition={{ delay: 0.3 }}>
        MCA @ VIPS-TC (GGSIPU) | AI/ML Engineer | Full-Stack Developer | Resume Analyzer Dev | Data Science Enthusiast | Placement Coordinator
      </motion.p>

      <motion.div initial={{ y: 50, opacity: 0 }} animate={{ y: 0, opacity: 1 }} transition={{ delay: 0.5 }}>
        <Tabs defaultValue="education">
          <TabsList className="flex flex-wrap gap-2">
            <TabsTrigger value="education">🎓 Education</TabsTrigger>
            <TabsTrigger value="experience">💼 Experience</TabsTrigger>
            <TabsTrigger value="internships">🎯 Internships</TabsTrigger>
            <TabsTrigger value="projects">🧪 Projects</TabsTrigger>
            <TabsTrigger value="awards">🏅 Achievements</TabsTrigger>
            <TabsTrigger value="extras">🎭 Activities</TabsTrigger>
          </TabsList>

          <TabsContent value="education">
            <ScrollArea className="h-64">
              <ul className="list-disc list-inside space-y-2">
                <li><strong>MCA</strong> - VIPS-TC (GGSIPU), 2023–2025, CGPA: 8.6</li>
                <li><strong>BSc (Hons) CS</strong> - SGTB Khalsa College, DU, 2020–2023, 70%</li>
                <li><strong>12th</strong> - DPS Rohini, CBSE, 2020, 97%</li>
                <li><strong>10th</strong> - DPS Rohini, CBSE, 2018, 93%</li>
              </ul>
            </ScrollArea>
          </TabsContent>

          <TabsContent value="experience">
            <ScrollArea className="h-64">
              <ul className="list-disc list-inside space-y-2">
                <li>Placement Coordinator @ VIPS-TC (2024–Present)</li>
                <li>Sales Executive @ Priyakarnı Trade & Leads Pvt Ltd (2023–Present)</li>
                <li>Sales Executive @ Priyakarnı Forex & Travels (2021–2023)</li>
                <li>Industry Visitor @ ZUBDHA Pvt Ltd (2023)</li>
                <li>Talent & Social Media Associate @ Celebrity Face Pvt Ltd (2018–2022)</li>
                <li>Tech Club Member @ XINO (201 6–2018)</li>
                <li>Theatre Artist @ National School of Drama (2016–2018)</li>
              </ul>
            </ScrollArea>
          </TabsContent>

          <TabsContent value="internships">
            <ScrollArea className="h-64">
              <ul className="list-disc list-inside space-y-2">
                <li>IBM SkillsBuild – Data Science Intern (Oct–Nov 2024)</li>
                <li>Oasis Infobyte – Data Science Intern (Sep–Oct 2024)</li>
              </ul>
            </ScrollArea>
          </TabsContent>

          <TabsContent value="projects">
            <ScrollArea className="h-64">
              <ul className="list-disc list-inside space-y-2">
                <li><a className="text-blue-500 underline" href="https://github.com/mehuljain133/Jarvis-Desktop-Voice-Assistant">Jarvis Desktop Voice Assistant</a></li>
                <li><a className="text-blue-500 underline" href="https://github.com/mehuljain133/Face_recognition_based_attendance_system">Face Recognition Attendance System</a></li>
                <li><a className="text-blue-500 underline" href="https://github.com/mehuljain133/Accounting-Software-using-ASP.NET-Core-Web-Development-Framework">Accounting Software in ASP.NET Core</a></li>
                <li><a className="text-blue-500 underline" href="https://github.com/mehuljain133/AI-Nexus">AI-Nexus</a></li>
                <li><a className="text-blue-500 underline" href="https://github.com/mehuljain133/AI-Resume-Analyzer-And-Builder">AI Resume Analyzer & Builder</a></li>
                <li><a className="text-blue-500 underline" href="https://github.com/mehuljain133/Github-Terminal">GitHub Terminal</a></li>
              </ul>
            </ScrollArea>
          </TabsContent>

          <TabsContent value="awards">
            <ScrollArea className="h-64">
              <ul className="list-disc list-inside space-y-2">
                <li>Certificate of Appreciation – Ministry of Culture</li>
                <li>Publication: Smart Attendance System with Face Recognition</li>
                <li>Developed and Deployed Full-stack Resume Analytics Tool</li>
                <li>Organized campus-wide tech and cultural events</li>
                <li>Top performer in coding challenges and data competitions</li>
              </ul>
            </ScrollArea>
          </TabsContent>

          <TabsContent value="extras">
            <ScrollArea className="h-64">
              <ul className="list-disc list-inside space-y-2">
                <li>Volunteer: Donation Drives, Campus Initiatives</li>
                <li>Tech Club (XINO), Theatre (NSD), Influencer Campaigns</li>
                <li>Hobbies: AI Audio/Video Editing, YouTube Content, Competitive Coding</li>
                <li>Sports: Cricket 🏏, Football ⚽, Badminton 🏸</li>
                <li>Other Interests: Productivity Tools, Startup Ideation, Tech for Good</li>
              </ul>
            </ScrollArea>
          </TabsContent>
        </Tabs>
      </motion.div>
    </div>
  );
}
