import React, { useState } from 'react'
import { motion } from 'framer-motion'
import Image from 'next/image'

// Utility function for formatting dates
const formatDate = (dateString: string) => {
  return new Date(dateString).toLocaleDateString('en-US', {
    year: 'numeric',
    month: 'long',
    day: 'numeric'
  })
}

// Header Component
const Header = () => (
  <header className="bg-white shadow-sm">
    <nav className="container mx-auto px-4 py-4 flex justify-between items-center">
      <a href="#" className="text-xl font-semibold text-gray-800">Dr. Jane Doe</a>
      <ul className="flex space-x-4">
        <li><a href="#" className="text-gray-600 hover:text-gray-800">Home</a></li>
        <li><a href="#projects" className="text-gray-600 hover:text-gray-800">Projects</a></li>
        <li><a href="#publications" className="text-gray-600 hover:text-gray-800">Publications</a></li>
        <li><a href="#presentations" className="text-gray-600 hover:text-gray-800">Presentations</a></li>
        <li><a href="#contact" className="text-gray-600 hover:text-gray-800">Contact</a></li>
      </ul>
    </nav>
  </header>
)

// Hero Component
const Hero = () => (
  <section className="container mx-auto px-4 text-center py-16">
    <h1 className="text-4xl font-bold mb-4">Dr. Jane Doe</h1>
    <h2 className="text-2xl text-gray-600 mb-6">Computer Science Researcher</h2>
    <p className="max-w-2xl mx-auto text-gray-700 mb-8">
      Exploring the frontiers of artificial intelligence and machine learning to solve complex real-world problems.
    </p>
    <a href="#contact" className="bg-blue-500 text-white px-6 py-2 rounded hover:bg-blue-600 transition-colors">
      Get in Touch
    </a>
  </section>
)

// Projects Component
const projects = [
  {
    id: "ai-climate-modeling",
    title: "AI-Driven Climate Modeling",
    description: "Developing machine learning models to improve climate change predictions and mitigation strategies.",
    fullDescription: "This project focuses on leveraging artificial intelligence and machine learning techniques to enhance climate modeling accuracy. By incorporating vast amounts of historical climate data and real-time sensor information, we aim to create more precise and adaptable climate models. These advanced models will help policymakers and researchers better understand climate change patterns, predict future scenarios with higher accuracy, and develop more effective mitigation strategies."
  },
  {
    id: "quantum-computing-algorithms",
    title: "Quantum Computing Algorithms",
    description: "Researching novel quantum algorithms for optimization problems in logistics and supply chain management.",
    fullDescription: "Our quantum computing research is centered on developing innovative algorithms to solve complex optimization problems in logistics and supply chain management. By harnessing the power of quantum superposition and entanglement, we aim to tackle NP-hard problems that are intractable for classical computers. This research has the potential to revolutionize industries by significantly improving efficiency in areas such as route optimization, resource allocation, and inventory management."
  },
  {
    id: "ethical-ai-framework",
    title: "Ethical AI Framework",
    description: "Creating a comprehensive framework for ethical considerations in AI development and deployment.",
    fullDescription: "The Ethical AI Framework project is dedicated to addressing the growing concerns surrounding the ethical implications of artificial intelligence. We are developing a comprehensive set of guidelines, best practices, and evaluation metrics to ensure that AI systems are designed and deployed with strong ethical considerations. This framework covers areas such as fairness, transparency, privacy, and accountability, aiming to foster trust in AI technologies and promote their responsible use across various sectors."
  }
]

const Projects = () => (
  <section id="projects" className="container mx-auto px-4 py-16">
    <h2 className="text-3xl font-bold mb-8 text-center">Research Projects</h2>
    <div className="grid md:grid-cols-2 lg:grid-cols-3 gap-8">
      {projects.map((project) => (
        <div key={project.id} className="bg-white p-6 rounded shadow transition-transform hover:scale-105">
          <h3 className="text-xl font-semibold mb-2">{project.title}</h3>
          <p className="text-gray-600 mb-4">{project.description}</p>
          <details>
            <summary className="cursor-pointer text-blue-500 hover:text-blue-600">Read more</summary>
            <p className="mt-2 text-gray-700">{project.fullDescription}</p>
          </details>
        </div>
      ))}
    </div>
  </section>
)

// Publications Component
const publications = [
  {
    title: "Machine Learning Approaches to Climate Model Uncertainty Reduction",
    journal: "Journal of Climate Informatics",
    year: 2023,
    thumbnail: "/placeholder.svg?height=80&width=80"
  },
  {
    title: "Quantum-Inspired Algorithms for NP-Hard Problems in Supply Chain Optimization",
    journal: "Quantum Computing and Logistics",
    year: 2022,
    thumbnail: "/placeholder.svg?height=80&width=80"
  },
  {
    title: "Ethical Considerations in Automated Decision-Making Systems",
    journal: "AI Ethics Journal",
    year: 2021,
    thumbnail: "/placeholder.svg?height=80&width=80"
  }
]

const Publications = () => {
  const [hoveredIndex, setHoveredIndex] = useState<number | null>(null)

  return (
    <section id="publications" className="container mx-auto px-4 py-16">
      <h2 className="text-3xl font-bold mb-8 text-center">Recent Publications</h2>
      <ul className="space-y-4">
        {publications.map((pub, index) => (
          <motion.li
            key={index}
            className="bg-white p-4 rounded shadow flex items-center relative overflow-hidden"
            onHoverStart={() => setHoveredIndex(index)}
            onHoverEnd={() => setHoveredIndex(null)}
          >
            <Image
              src={pub.thumbnail || "/placeholder.svg"}
              alt={`Thumbnail for ${pub.title}`}
              width={80}
              height={80}
              className="mr-4 rounded-lg"
            />
            <div className="flex-grow">
              <h3 className="font-semibold">{pub.title}</h3>
              <p className="text-gray-600">{pub.journal}, {pub.year}</p>
            </div>
            {hoveredIndex === index && (
              <motion.div
                className="w-2 h-full bg-blue-500 absolute left-0 top-0"
                initial={{ scaleY: 0 }}
                animate={{ scaleY: 1 }}
                transition={{ duration: 0.2 }}
              />
            )}
          </motion.li>
        ))}
      </ul>
    </section>
  )
}

// Presentations Component
const presentations = [
  {
    title: "The Future of AI in Climate Science",
    event: "Global Climate Conference",
    date: "2023-05-15",
    youtubeId: "dQw4w9WgXcQ"
  },
  {
    title: "Quantum Computing: A New Era in Optimization",
    event: "International Quantum Symposium",
    date: "2022-11-03",
    youtubeId: "dQw4w9WgXcQ"
  },
  {
    title: "Ethics in AI: Challenges and Solutions",
    event: "AI Ethics Forum",
    date: "2022-09-22",
    youtubeId: "dQw4w9WgXcQ"
  }
]

const Presentations = () => (
  <section id="presentations" className="container mx-auto px-4 py-16">
    <h2 className="text-3xl font-bold mb-8 text-center">Presentations</h2>
    <ul className="space-y-4">
      {presentations.map((presentation, index) => (
        <li key={index} className="bg-white p-4 rounded shadow flex items-center">
          <a href={`https://www.youtube.com/watch?v=${presentation.youtubeId}`} target="_blank" rel="noopener noreferrer">
            <Image
              src={`https://img.youtube.com/vi/${presentation.youtubeId}/0.jpg`}
              alt={`Thumbnail for ${presentation.title}`}
              width={120}
              height={90}
              className="mr-4 rounded-lg transition-transform hover:scale-105"
            />
          </a>
          <div>
            <h3 className="font-semibold">{presentation.title}</h3>
            <p className="text-gray-600">{presentation.event}</p>
            <p className="text-gray-500">{formatDate(presentation.date)}</p>
          </div>
        </li>
      ))}
    </ul>
  </section>
)
