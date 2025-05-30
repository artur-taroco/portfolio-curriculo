<template>
  <section class="text-center space-y-8">
    <div class="max-w-4xl mx-auto">
      <h1 class="text-4xl md:text-5xl font-bold mb-6 text-gray-800">
        Olá! Eu sou <span class="text-blue-600">Artur Taroco</span>
      </h1>
      <p class="text-xl text-gray-600 mb-8">
        Estudante de Análise e Desenvolvimento de Sistemas com interesse em desenvolvimento web
      </p>
      
      <div class="flex flex-col sm:flex-row gap-4 justify-center mb-12">
        <a 
          href="#projetos" 
          class="bg-blue-600 text-white px-6 py-3 rounded-lg hover:bg-blue-700 transition-colors"
        >
          Ver Meus Projetos
        </a>
        <router-link 
          to="/contato" 
          class="border border-blue-600 text-blue-600 px-6 py-3 rounded-lg hover:bg-blue-50 transition-colors"
        >
          Entre em Contato
        </router-link>
      </div>
    </div>

    <div class="grid grid-cols-1 md:grid-cols-3 gap-6 max-w-4xl mx-auto">
      <div class="bg-white p-6 rounded-lg shadow-sm">
        <h3 class="font-semibold text-gray-800 mb-2">Estudante de ADS</h3>
        <p class="text-gray-600 text-sm">Cursando Análise e Desenvolvimento de Sistemas na UNIMAR</p>
      </div>
      
      <div class="bg-white p-6 rounded-lg shadow-sm">
        <h3 class="font-semibold text-gray-800 mb-2">Desenvolvedor em Formação</h3>
        <p class="text-gray-600 text-sm">Focado em tecnologias backend</p>
      </div>
      
      <div class="bg-white p-6 rounded-lg shadow-sm">
        <h3 class="font-semibold text-gray-800 mb-2">Sempre Aprendendo</h3>
        <p class="text-gray-600 text-sm">Busco sempre aprender cada vez mais</p>
      </div>
    </div>

    <div id="projetos" class="space-y-6 mt-16">
      <div class="text-center mb-8">
        <h2 class="text-3xl font-bold text-gray-800 mb-2">Meus Projetos</h2>
        <p class="text-gray-600">Alguns projetos que desenvolvi durante minha jornada de aprendizado</p>
      </div>
      
      <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6 max-w-6xl mx-auto">
        <ComponentsProjeto 
          v-for="project in projects" 
          :key="project.id"
          :project="project"
        />
      </div>
      
      <div class="text-center mt-8 p-6 bg-blue-50 rounded-lg max-w-4xl mx-auto">
        <h3 class="text-lg font-semibold text-gray-800 mb-2">Mais projetos em desenvolvimento</h3>
        <p class="text-gray-600">Estou sempre trabalhando em novos projetos. Confira meu GitHub para ver as atualizações mais recentes!</p>
        <a 
          href="https://github.com/artur-taroco" 
          target="_blank"
          class="inline-block mt-3 px-4 py-2 bg-blue-600 text-white rounded hover:bg-blue-700 transition-colors"
        >
          Visitar GitHub
        </a>
      </div>
    </div>
  </section>
</template>

<script setup>
import { ref } from 'vue'
import ProjectCard from '../components/ComponentsProjeto.vue'
import ComponentsProjeto from '../components/ComponentsProjeto.vue';

const projects = ref([
  {
    id: 1,
    title: "Portfólio Pessoal",
    description: "Site pessoal desenvolvido com Vue 3 para apresentar meus projetos e habilidades de forma organizada.",
    technologies: ["Vue 3", "Vue Router", "Tailwind CSS", "Vite"],
    status: "Concluído",
    githubUrl: "https://github.com/artur-taroco/portfolio-curriculo",
    liveUrl: "#"
  },
  {
    id: 2,
    title: "Sistema de Gerenciamento",
    description: "Aplicação web para gerenciamento de dados com interface intuitiva e design responsivo.",
    technologies: ["JavaScript", "HTML", "CSS", "Local Storage"],
    status: "Em desenvolvimento",
    githubUrl: "https://github.com/artur-taroco/gerenciador-financeiro"
  },
  {
    id: 3,
    title: "Landing Page Responsiva",
    description: "Página de apresentação moderna e totalmente responsiva desenvolvida para uma empresa fictícia.",
    technologies: ["HTML5", "CSS3", "JavaScript", "Bootstrap"],
    status: "Concluído",
    githubUrl: "https://github.com/artur-taroco/landing-page",
    liveUrl: "#"
  },
  {
    id: 4,
    title: "Aplicativo de Tarefas",
    description: "Aplicação simples para gerenciamento de tarefas diárias com funcionalidades completas de CRUD.",
    technologies: ["Vue.js", "Vuex", "CSS3"],
    status: "Planejado",
    githubUrl: "https://github.com/artur-taroco/todolist1"
  }
])
</script>
