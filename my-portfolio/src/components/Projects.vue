<template>
  <section id="projects" class="projects-section py-16 px-8">
    <h2 class="text-4xl font-bold text-gray-900 mb-10 text-left">Projects</h2>

    <!-- Projects container -->
    <div class="projects-container">
      <div 
        v-for="(project, index) in projects" 
        :key="index"
        class="project-item opacity-0 transition-opacity duration-1000 ease-in-out"
        :class="{'fade-in': project.show}"
      >
        <!-- Left Side: Project text -->
        <div class="project-text w-full md:w-1/2 text-left">
          <h3 class="text-3xl font-semibold text-gray-800">{{ project.title }}</h3>
          <p class="text-sm text-gray-600">{{ project.task }}</p>
          <p class="mt-4 text-lg text-gray-700">{{ project.problem }}</p>
          <p class="mt-4 text-lg text-gray-700">{{ project.solution }}</p>
          <p class="text-sm text-gray-600">{{ project.role }}</p>
        </div>
        
        <!-- Right Side: Image Slider -->
        <div class="project-image w-full md:w-1/2">
          <!-- Image Slider -->
          <div class="image-slider overflow-hidden relative">
            <div class="slider-images flex transition-all duration-500 ease-in-out">
              <img v-for="(image, imgIndex) in project.images" :key="imgIndex" :src="image" alt="project image" class="slider-image w-full h-auto object-contain" />
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  data() {
    return {
      projects: [
        {
          title: "Our Planet Free of Plastic",
          task: "Branding | Logo | Visual Identity | Web development",
          role: "MY ROLE: Graphic designer, content developer, brand strategist",
          problem: "PROBLEM: Plastic pollution is one of the most pressing environmental issues of our time, affecting oceans, wildlife, and human health. The project aimed to develop a campaign and brand identity designed to inspire people to support and sign the Global Plastic Treaty.",
          solution: "SOLUTION: Developed a Style Guide, posters, promotional videos, and an interactive website to raise awareness about the Global Plastic Treaty.",
          images: ["/visuals/project1.jpeg", "/visuals/project1.3.jpeg", "/visuals/project1.1.png"], 
          show: false
        },
        {
          title: "Esbjerg City Guide",
          task: "Poster layout | Booklet design | Illustrations",
          role: "MY ROLE: Creative director, graphic designer",
          problem: "PROBLEM: The city needed a visually engaging and informative guide to its tourist attractions, to make it easier for visitors to discover and explore its key landmarks. The goal was to create an informative and visually appealing design that would attract tourists and encourage exploration.",
          solution: "SOLUTION: Created a visually engaging poster showcasing the top attractions and landmarks to capture the attention of tourists and locals alike. Developed a tourist booklet with the highlighted must-see sites, and provided useful tips for visitors. Incorporated local branding by using colors and typography inspired by the city’s culture and identity. ",
          images: ["/visuals/book2.png", "/visuals/posterE.jpeg"],
          show: false
        },
    
        {
          title: "Esbjerg City Branding",
          task: "SoMe Campaign | Marketing | Brand strategy",
          role: "MY ROLE: Marketing strategist, graphic designer",
          problem: "PROBLEM: Esbjerg has often been seen as an industrial harbor town, lacking the cultural appeal that attracts international students. Despite its natural beauty and growing creative scene, the city’s image hasn’t caught up. There was a need to rebrand the city and engage its international community more meaningfully.",
          solution: "SOLUTION: We developed a targeted campaign and engagement strategy to rebrand Esbjerg as a cultural, beautiful, and international-friendly city. As a key part of the campaign, we planned an Open Day event for international students, including cultural activities and a creative storytelling workshop. This experience allows students to connect with the city and share their own stories, which we amplified through digital content. The strategy helped shift the narrative—showcasing Esbjerg as not just a place to study, but a place to belong.",
          images: ["/visuals/MOCKUP.png", "/visuals/EsbjergOpenDay2.jpg" ],
          show: false
        },
        {
          title: "The Lab",
          task: "Logo design | Poster layout | Concept development",
          role: "MY ROLE: Marketing strategist, graphic designer",
          problem: "PROBLEM: The university's creative needed a brand identity to differentiate from other departments and communicate its services to students, faculty, and staff. The goal was to create a professional, recognizable brand that conveyed the lab’s role as a valuable resource for students at EASV. ",
          solution: "SOLUTION: • Logo design: Developed different logo variations that represents the printing lab’s services while maintaining a professional and modern aesthetic. Created a poster to showcase the lab's services, such as 3d printing, embroidery and heat press. Developed a promotional video for Social Media use in After Effects.",
          images: ["/visuals/project3.jpg", "/visuals/Thelab_info.png", "/visuals/Thelab_bag.png"],
          show: false
        },
        {
          title: "Style Guide EASV",
          task: "Branding | Visual identity | Logo design ",
          role: "MY ROLE: Graphic designer, brand strategist",
          problem: "PROBLEM: Without clear guidance, many struggled to apply the university’s visual identity correctly, resulting in improper logo usage, color inconsistencies, and branding misalignment. ",
          solution: "SOLUTION: I redesigned the university’s style guide to make it more accessible and user-friendly. The new version provides clear, structured guidelines on brand application while ensuring ease of use for students, faculty, and staff. Key enhancements include: A centralized resource with all logo variations, color palettes, and typography files available for direct download in the guide. ",
          images: ["/visuals/Style.jpeg", "/visuals/project2.2.jpeg" ],
          show: false
        },
        {
          title: "Mobile app HappILY",
          task: "App design | Concept development | UX/UI design ",
          role: "MY ROLE: UX/UI designer, graphic designer",
          problem: "PROBLEM:Many students and individuals in need struggle to access mental health resources due to financial barriers, and complex digital platforms. The aim was to develop a user-friendly, affordable, and accessible mental health app that provides support, guidance, and interactive tools for mental well-being.",
          solution: "SOLUTION: User-friendly App Design: The app features a clean, intuitive interface. Special attention was given to navigation simplicity, calming visual aesthetics, ensuring that users can engage with the platform comfortably. The app includes self-assessment tools to help users understand their mental state through quick, accessible quizzes. Based on results, the app recommends personalized content and guidance. To enhance user engagement and emotional resonance, I developed a set of illustrations. The art style is intentionally soft and relatable.",
          images: ["/visuals/project5.png", "/visuals/AppMockup.png" ],
          show: false
        },
      ]
    };
  },
  mounted() {
    // Set up Intersection Observer to track when projects come into view
    const options = {
      root: null, // Use the viewport as the root
      threshold: 0.1, // Trigger when 10% of the element is visible
    };
  
    const observer = new IntersectionObserver(this.handleIntersection, options);
  
    // Observe each project item
    this.$nextTick(() => {
      const projectItems = this.$el.querySelectorAll('.project-item');
      projectItems.forEach(item => observer.observe(item));
    });
  },
  methods: {
    handleIntersection(entries) {
      entries.forEach(entry => {
        if (entry.isIntersecting) {
          entry.target.classList.add('fade-in');
          entry.target.classList.remove('opacity-0');
        }
      });
    },
  },
};
</script>

<style scoped>
.projects-section {
  background-color: #f9fafb;
}

.projects-container {
  display: flex;
  flex-direction: column;
  gap: 50px;
}

.project-item {
  display: flex;
  align-items: center;
  justify-content: space-between;
  opacity: 0; /* Initially hidden */
  transition: opacity 0.5s ease-in-out;
  padding: 40px;
}

.project-text {
  max-width: 50%;
  padding-right: 20px;
}

.project-image {
  width: 100%;
  display: flex;
  justify-content: center;
}

.image-slider {
  width: 100%;
  overflow: hidden;
}

.slider-images {
  display: flex;
  transition: transform 0.3s ease-in-out;
}

.slider-image {
  width: 100%;
  object-fit: contain;
  max-height: 300px; /* You can adjust the height of the image */
  transition: transform 0.3s ease, opacity 0.3s ease; /* Add transition for both scale and fade */
}

.slider-image:hover {
  transform: scale(1.05); /* Zoom-in effect on hover */
}

.fade-in {
  opacity: 1;
}

/* Add scroll-based effect */
@media (min-width: 768px) {
  .projects-container {
    flex-direction: column;
  }

  .project-item {
    flex-direction: row; /* Align text and image side by side on larger screens */
  }

  .project-text {
    padding-right: 50px;
  }
}

/* Mobile styling (max-width: 768px) */
@media (max-width: 768px) {
  .projects-container {
    flex-direction: column; /* Stack projects vertically */
  }

  .project-item {
    flex-direction: column; /* Stack text and images vertically */
  }

  .project-text {
    max-width: 100%; /* Make sure text takes up full width on mobile */
    padding-right: 0; /* Remove right padding */
  }

  .project-image {
    width: 100%; /* Make sure image container takes up full width on mobile */
    margin-top: 1rem; /* Add space between text and images */
  }

  .slider-image {
    max-height: 250px; /* Optionally, reduce max height of images on mobile */
    margin-bottom: 1rem; /* Add spacing between images */
  }
}
</style>
