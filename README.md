"use client"
import { useState } from "react"
import { ChevronDown } from "lucide-react"
import Link from "next/link"

interface PublicationProps {
  title: string
  authors: string
  venue: string
  institution?: string
  details?: string
  date: string
  links: { label: string; url: string }[]
  abstract?: string
  isAbstractOpen: boolean
  onAbstractToggle: () => void
}

function PublicationPanel({
  title,
  authors,
  venue,
  institution,
  details,
  date,
  links,
  abstract,
  isAbstractOpen,
  onAbstractToggle,
}: PublicationProps) {
  return (
    <div className="max-w-4xl mx-auto mb-8 space-y-2">
      {/* Title */}
      <h3 className="text-lg font-semibold text-gray-900 leading-tight">{title}</h3>

      {/* Authors */}
      <div className="text-base text-gray-900" dangerouslySetInnerHTML={{ __html: authors }} />

      {/* Venue */}
      <div className="text-base italic text-gray-900">{venue}</div>

      {/* Institution */}
      {institution && <div className="text-base italic text-gray-900">{institution}</div>}

      {/* Details */}
      {details && <div className="text-base text-gray-900">{details}</div>}

      {/* Date */}
      <div className="text-base text-[#005A92]">{date}</div>

      {/* Abstract dropdown */}
      {abstract && (
        <div className="mt-4">
          <button
            onClick={onAbstractToggle}
            className="flex items-center gap-2 text-base font-medium text-gray-900 hover:text-gray-700 transition-colors"
          >
            <span>abstract</span>
            <ChevronDown
              className={`w-4 h-4 transition-transform duration-200 ${isAbstractOpen ? "rotate-180" : ""}`}
            />
          </button>

          {/* Abstract content */}
          <div
            className={`overflow-hidden transition-all duration-300 ${
              isAbstractOpen ? "max-h-96 opacity-100 mt-4" : "max-h-0 opacity-0"
            }`}
          >
            <div className="text-base text-gray-800 leading-relaxed">
              <p>{abstract}</p>
            </div>
          </div>
        </div>
      )}

      {/* Links */}
      <div className="flex gap-1 text-base">
        {links.map((link, index) => (
          <span key={index}>
            <span className="text-gray-900">[</span>
            <Link href={link.url} target="_blank" className="text-blue-600 hover:text-blue-800 underline">
              {link.label}
            </Link>
            <span className="text-gray-900">]</span>
            {index < links.length - 1 && <span className="text-gray-900"> </span>}
          </span>
        ))}
      </div>
    </div>
  )
}

export default function Portfolio() {
  const [openAbstracts, setOpenAbstracts] = useState<Set<string>>(new Set())

  const toggleAbstract = (id: string) => {
    const newOpen = new Set(openAbstracts)
    if (newOpen.has(id)) {
      newOpen.delete(id)
    } else {
      newOpen.add(id)
    }
    setOpenAbstracts(newOpen)
  }

  const publications = [
    {
      id: "pub-1",
      title: "AI-Powered VR Simulations for Semiconductor Industry Training and Education",
      authors:
        '<span style="color: #ff1423; font-weight:bold;">I. Jha</span>, G. Codina, A. Dong, K. Hong, A. Rodriguez, F. Chen, J. Zhu, G.P Li',
      venue: "Journal of Advanced Technological Education",
      date: "Accepted November 27, 2024",
      abstract:
        "We present an innovative approach to semiconductor industry training through AI-powered virtual reality simulations. Our system combines advanced artificial intelligence algorithms with immersive VR technology to create realistic training environments for semiconductor manufacturing processes. The platform provides hands-on experience in cleanroom operations, equipment handling, and safety protocols without the risks and costs associated with traditional training methods.",
      links: [
        { label: "paper", url: "https://zenodo.org/records/14933891" },
        { label: "video demo", url: "https://www.youtube.com/watch?v=Ri-jqU0WzQM&t=5s" },
        { label: "NSF feature", url: "https://www.nsf.gov/news/sparking-curiosity-future-semiconductor-workforce" },
      ],
    },
  ]

  const presentations = [
    {
      id: "pres-1",
      title: "AI For Education and Training",
      authors:
        '<span style="color: #ff1423; font-weight:bold;">Ishan Jha, </span>K. Hong, N. Vatanshenas, A. Ashcroft, A. Ahmadi, R. Almache, R. Dhar, H. Mandadi, R.D. Melara, J.J. Mosquera, P.K. Stout, B. Harrop',
      venue: "TechConnect Word Conference",
      institution: "University of California, Irvine ; Princeton University",
      details: "Poster and Invited Talk, J.W Marriot Austin",
      date: "June 9-11, 2025",
      abstract:
        "This presentation explores the transformative potential of artificial intelligence in educational settings and professional training environments. We discuss innovative AI applications that enhance learning outcomes, personalize educational experiences, and provide scalable training solutions across various industries.",
      links: [{ label: "poster", url: "https://princeton.edu" }],
    },
    {
      id: "pres-2",
      title: "Agentic AI-embedded Digital Twins for Semiconductor Manufacturing Education",
      authors:
        '<span style="color: #ff1423; font-weight:bold;">Ishan Jha,</span> Kristal Hong, Nick Vatanshenas, Adam Ashcroft',
      venue: "California Institute of Technology",
      institution: "Kavli Nanoscience Institute",
      details: "Poster Presentation, Moore Courtyard",
      date: "May 30, 2025",
      abstract:
        "We introduce a novel approach to semiconductor manufacturing education through agentic AI-embedded digital twins. Our system creates intelligent virtual representations of manufacturing processes that can autonomously adapt and respond to different educational scenarios, providing students with dynamic and interactive learning experiences.",
      links: [
        {
          label: "poster",
          url: "https://github.com/Ishanyjha/ishanyjha.github.io/blob/b8a08e5515cd70a42ba76ed5155820049a36e841/Poster%20for%20Caltech%202025.pdf",
        },
      ],
    },
    {
      id: "pres-3",
      title: "AI For Education and Training",
      authors: '<span style="color: #ff1423; font-weight:bold;">Ishan Jha</span>, Others',
      venue: "Orange County Department of Education",
      institution: "Future Leaders AI Conference",
      details: "Presentation, J.W Marriot",
      date: "November 20, 2024",
      links: [
        {
          label: "slides",
          url: "https://docs.google.com/presentation/d/1trymELfKDnHdj340TnMqMLKF8STPKpN9xWVmITHn03Y/edit?usp=sharing",
        },
      ],
    },
    {
      id: "pres-4",
      title: "Student Centered Undergraduate Research Experiences in Creating Virtual Digital Twin Cleanroom.",
      authors:
        '<span style="color: #ff1423; font-weight:bold;">Ishan Jha</span>, Gabriel Codina, Alice Dong, Kristal Hong',
      venue: "TechConnect World Innovation Conference",
      institution: "XRAI for Training Symposium",
      details: "Poster presentation and panel, The Gaylord National Hotel",
      date: "June 16-17, 2024",
      links: [
        {
          label: "poster",
          url: "https://github.com/Ishanyjha/ishanyjha.github.io/blob/2c21d5897545eb75615c337f28bb3d09b966de41/UCI%20START%20Academic%20Poster%20(1).pdf",
        },
      ],
    },
    {
      id: "pres-5",
      title: "Digital Twins for Semiconductor Fabrication Education.",
      authors:
        '<span style="color: #ff1423; font-weight:bold;">Ishan Jha</span>, Gabriel Codina, Alice Dong, Kristal Hong, Felicia Chen',
      venue: "California Institute of Technology",
      institution: "Kavli Nanoscience Institute",
      details: "Poster and presentation, Moore Courtyard and EECS Bldg.",
      date: "May 24, 2024",
      links: [
        {
          label: "poster",
          url: "https://github.com/Ishanyjha/ishanyjha.github.io/blob/2c21d5897545eb75615c337f28bb3d09b966de41/UCI%20START%20Academic%20Poster%20(1).pdf",
        },
      ],
    },
    {
      id: "pres-6",
      title: "Empowering Students Through AI Clubs",
      authors: '<span style="color: #ff1423; font-weight:bold;">Ishan Jha</span>',
      venue: "Orange County Department of Education",
      institution: "Student AI Convening",
      details: "Presentation, J.W Marriot",
      date: "May 4, 2024",
      links: [
        {
          label: "slides",
          url: "https://docs.google.com/presentation/d/1hj7_zbnqVg7TAxt5kjAVCEwvPyUrD_DBp5Ijl_JvQo8/edit?usp=sharing",
        },
        { label: "video", url: "https://www.youtube.com/watch?v=NugQOMaJuuw" },
      ],
    },
  ]

  return (
    <div className="min-h-screen bg-white font-sans">
      {/* Navigation Bar */}
      <nav className="bg-white border-b border-gray-200 px-6 py-4">
        <div className="max-w-6xl mx-auto flex justify-between items-center">
          <Link href="/" className="text-xl font-bold text-gray-900 no-underline">
            Ishan Jha
          </Link>
          <div className="flex gap-6">
            <Link href="/projects" className="text-gray-700 hover:text-gray-900 no-underline">
              Projects
            </Link>
            <Link
              href="https://scholar.google.com/citations?user=KJxBoMAAAAAJ&hl=en&"
              target="_blank"
              className="text-gray-700 hover:text-gray-900 no-underline"
            >
              Google Scholar
            </Link>
            <Link
              href="https://github.com/ishanyjha"
              target="_blank"
              className="text-gray-700 hover:text-gray-900 no-underline"
            >
              GitHub
            </Link>
          </div>
        </div>
      </nav>

      <div className="max-w-6xl mx-auto px-6 py-8">
        {/* Introduction */}
        <section className="mb-12">
          <h1 className="text-3xl font-bold text-center mb-6">Welcome!</h1>
          <div className="space-y-4 text-gray-800 leading-relaxed max-w-4xl mx-auto">
            <p>Greetings, I am a ninth grader at Troy High School in Fullerton, California.</p>
            <p>
              My passions are theoretical mathematics, artificial intelligence, and its applications. Within artificial
              intelligence, I am currently exploring computer vision and physics-informed neural networks through
              literature and projects. I also enjoy studying the applications of these ideas in machine learning and
              industry.
            </p>
            <p>
              Another passion of mine is conducting academic research, helping students with math at the UCI Math
              Circle, and presenting at conferences in AI. I love connecting with like minded people who are interested
              in AI, math, and research!
            </p>
          </div>
        </section>

        {/* Publications Section */}
        <section className="mb-12">
          <h2 className="text-2xl font-bold text-center mb-8">Publications</h2>
          {publications.map((pub) => (
            <PublicationPanel
              key={pub.id}
              title={pub.title}
              authors={pub.authors}
              venue={pub.venue}
              institution={pub.institution}
              details={pub.details}
              date={pub.date}
              links={pub.links}
              abstract={pub.abstract}
              isAbstractOpen={openAbstracts.has(pub.id)}
              onAbstractToggle={() => toggleAbstract(pub.id)}
            />
          ))}
        </section>

        {/* Presentations Section */}
        <section className="mb-12">
          <h2 className="text-2xl font-bold text-center mb-8">Presentations</h2>
          {presentations.map((pres) => (
            <PublicationPanel
              key={pres.id}
              title={pres.title}
              authors={pres.authors}
              venue={pres.venue}
              institution={pres.institution}
              details={pres.details}
              date={pres.date}
              links={pres.links}
              abstract={pres.abstract}
              isAbstractOpen={openAbstracts.has(pres.id)}
              onAbstractToggle={() => toggleAbstract(pres.id)}
            />
          ))}
        </section>
      </div>

      {/* Footer */}
      <footer className="mt-16 p-6 bg-gray-800 text-white text-center rounded-lg mx-6">
        <p className="font-bold">Copyright © 2025 Ishan Jha</p>
      </footer>
    </div>
  )
}
