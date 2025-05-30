<template>
  <section class="space-y-8">
    <div class="text-center mb-8">
      <h1 class="text-3xl font-bold text-gray-800 mb-4">Sobre Mim</h1>
      <div class="max-w-3xl mx-auto">
        <p class="text-lg text-gray-700 mb-4">
          Meu nome é Artur Taroco, tenho 19 anos e sou estudante de Análise e Desenvolvimento 
          de Sistemas na Universidade de Marília. Tenho grande interesse por tecnologia e 
          desenvolvimento web.
        </p>
        <p class="text-gray-600">
          Gosto de trabalhar em equipe, estou sempre disposto a aprender coisas novas e 
          meu objetivo é contribuir para projetos que façam diferença. Busco constantemente 
          aprimorar minhas habilidades técnicas e interpessoais.
        </p>
      </div>
    </div>

    <div class="bg-gray-50 rounded-lg p-6">
      <h2 class="text-2xl font-semibold text-gray-800 mb-8 text-center">Experiencias / Escolaridade</h2>
      <div class="max-w-3xl mx-auto">
        <ComponentsExperiencia 
          v-for="(item, index) in timeline" 
          :key="item.id"
          :item="item"
          :isLast="index === timeline.length - 1"
        />
      </div>
    </div>

    <div class="bg-white rounded-lg shadow-sm p-6">
      <h2 class="text-2xl font-semibold text-gray-800 mb-6 text-center">Habilidades</h2>
      <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6">
        <div class="space-y-3">
          <h3 class="font-semibold text-gray-700">Técnicas</h3>
          <div class="space-y-2">
            <div class="flex justify-between items-center">
              <span class="text-sm">HTML/CSS</span>
              <div class="w-24 bg-gray-200 rounded-full h-2">
                <div class="bg-blue-600 h-2 rounded-full" style="width: 85%"></div>
              </div>
            </div>
            <div class="flex justify-between items-center">
              <span class="text-sm">JavaScript</span>
              <div class="w-24 bg-gray-200 rounded-full h-2">
                <div class="bg-blue-600 h-2 rounded-full" style="width: 75%"></div>
              </div>
            </div>
            <div class="flex justify-between items-center">
              <span class="text-sm">Vue.js</span>
              <div class="w-24 bg-gray-200 rounded-full h-2">
                <div class="bg-blue-600 h-2 rounded-full" style="width: 70%"></div>
              </div>
            </div>
          </div>
        </div>
        
        <div class="space-y-3">
          <h3 class="font-semibold text-gray-700">Interpessoais</h3>
          <ul class="text-sm text-gray-600 space-y-1">
            <li>• Comunicação eficaz</li>
            <li>• Trabalho em equipe</li>
            <li>• Proatividade</li>
            <li>• Organização</li>
          </ul>
        </div>
        
        <div class="space-y-3">
          <h3 class="font-semibold text-gray-700">Ferramentas</h3>
          <ul class="text-sm text-gray-600 space-y-1">
            <li>• Git/GitHub</li>
            <li>• VS Code</li>
            <li>• Figma (básico)</li>
            <li>• Tailwind CSS</li>
          </ul>
        </div>
      </div>
    </div>

    <div class="bg-white rounded-lg shadow-sm p-6">
      <h2 class="text-2xl font-semibold text-gray-800 mb-6 text-center">Currículo</h2>
      <div class="max-w-3xl mx-auto space-y-6">
        <div class="text-center border-b pb-4">
          <h3 class="text-xl font-bold">Artur Camilo Taroco</h3>
          <p class="text-gray-600">(14) 99891-5080 • arturtaroco5708@gmail.com</p>
          <p class="text-gray-600">Rua São Luís, 336 - Marília, SP • 11/01/2006</p>
          <a href="https://github.com/artur-taroco" target="_blank" class="text-blue-600 hover:underline">
            GitHub: github.com/artur-taroco
          </a>
        </div>
        
        <div>
          <h4 class="font-semibold text-gray-800 mb-2">Objetivo</h4>
          <p class="text-gray-700 text-sm">
            Busco uma oportunidade para desenvolver-me profissionalmente na área de tecnologia, 
            contribuindo com meu conhecimento e aprendendo constantemente.
          </p>
        </div>
        
        <div>
          <h4 class="font-semibold text-gray-800 mb-2">Formação</h4>
          <ul class="text-sm text-gray-700 space-y-1">
            <li>• Colégio Interação - Ensino Médio completo (2023)</li>
            <li>• Universidade de Marília - Cursando Análise e Desenvolvimento de Sistemas</li>
          </ul>
        </div>
        
        <div>
          <h4 class="font-semibold text-gray-800 mb-2">Experiência</h4>
          <p class="text-sm text-gray-700">
            <strong>21/03/2022 - Presente:</strong> IAT Alimentação LTDA<br />
            <em>Atendimento ao cliente - Desenvolvimento de habilidades de comunicação e trabalho em equipe</em>
          </p>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import { ref } from 'vue'
import ComponentsExperiencia from '../components/ComponentsExperiencia.vue'

const timeline = ref([
  {
    id: 1,
    title: "Análise e Desenvolvimento de Sistemas",
    institution: "Universidade de Marília (UNIMAR)",
    period: "2024 - Presente",
    description: "Cursando graduação tecnológica com foco em desenvolvimento de software, banco de dados e gestão de projetos.",
    achievements: [
      "Aprendendo programação orientada a objetos",
      "Desenvolvendo projetos práticos",
      "Estudando metodologias ágeis"
    ]
  },
  {
    id: 2,
    title: "Atendente",
    institution: "IAT Alimentação LTDA",
    period: "Março 2022 - Presente",
    description: "Responsável pelo atendimento ao cliente, desenvolvendo habilidades de comunicação e trabalho sob pressão.",
    achievements: [
      "Aprimoramento da comunicação interpessoal",
      "Experiência em trabalho sob pressão",
      "Desenvolvimento de proatividade"
    ]
  },
  {
    id: 3,
    title: "Ensino Médio",
    institution: "Colégio Interação",
    period: "2020 - 2023",
    description: "Conclusão do ensino médio com preparação para o ensino superior e descoberta do interesse por tecnologia.",
    achievements: [
      "Formação completa",
      "Participação em projetos escolares",
      "Desenvolvimento de interesse por tecnologia"
    ]
  }
])
</script>
