<template>
  <div class="max-w-6xl mx-auto space-y-8 py-8">
    <div class="text-center mb-12">
      <h1 class="text-4xl font-bold text-gray-900 mb-4">Electronics</h1>
      <p class="text-xl text-gray-600">
        Cutting-edge electronic components and solutions for modern industries
      </p>
    </div>

    <div class="grid md:grid-cols-2 lg:grid-cols-3 gap-8">
      <div class="bg-white p-6 rounded-lg shadow-sm border border-gray-200">
        <div class="w-12 h-12 bg-blue-100 rounded-lg flex items-center justify-center mb-4">
          <Icon name="i-heroicons-cpu-chip" class="w-6 h-6 text-blue-600" />
        </div>
        <h3 class="text-lg font-semibold mb-2">Semiconductors</h3>
        <p class="text-gray-600">
          Advanced semiconductor components for computing and industrial applications.
        </p>
      </div>

      <div class="bg-white p-6 rounded-lg shadow-sm border border-gray-200">
        <div class="w-12 h-12 bg-green-100 rounded-lg flex items-center justify-center mb-4">
          <Icon name="i-heroicons-circuit-board" class="w-6 h-6 text-green-600" />
        </div>
        <h3 class="text-lg font-semibold mb-2">Circuit Boards</h3>
        <p class="text-gray-600">
          High-quality PCBs and circuit boards for electronic manufacturing.
        </p>
      </div>

      <div class="bg-white p-6 rounded-lg shadow-sm border border-gray-200">
        <div class="w-12 h-12 bg-purple-100 rounded-lg flex items-center justify-center mb-4">
          <Icon name="i-heroicons-microchip" class="w-6 h-6 text-purple-600" />
        </div>
        <h3 class="text-lg font-semibold mb-2">Microcontrollers</h3>
        <p class="text-gray-600">
          Programmable microcontrollers for automation and IoT solutions.
        </p>
      </div>

      <div class="bg-white p-6 rounded-lg shadow-sm border border-gray-200">
        <div class="w-12 h-12 bg-yellow-100 rounded-lg flex items-center justify-center mb-4">
          <Icon name="i-heroicons-light-bulb" class="w-6 h-6 text-yellow-600" />
        </div>
        <h3 class="text-lg font-semibold mb-2">LED Components</h3>
        <p class="text-gray-600">
          Energy-efficient LED solutions for lighting and display applications.
        </p>
      </div>

      <div class="bg-white p-6 rounded-lg shadow-sm border border-gray-200">
        <div class="w-12 h-12 bg-red-100 rounded-lg flex items-center justify-center mb-4">
          <Icon name="i-heroicons-battery-100" class="w-6 h-6 text-red-600" />
        </div>
        <h3 class="text-lg font-semibold mb-2">Power Systems</h3>
        <p class="text-gray-600">
          Reliable power supplies and battery management systems.
        </p>
      </div>

      <div class="bg-white p-6 rounded-lg shadow-sm border border-gray-200">
        <div class="w-12 h-12 bg-indigo-100 rounded-lg flex items-center justify-center mb-4">
          <Icon name="i-heroicons-wifi" class="w-6 h-6 text-indigo-600" />
        </div>
        <h3 class="text-lg font-semibold mb-2">Wireless Solutions</h3>
        <p class="text-gray-600">
          Advanced wireless communication modules and IoT connectivity.
        </p>
      </div>
    </div>

    <section class="bg-gray-50 p-8 rounded-lg">
      <h2 class="text-2xl font-semibold mb-6 text-center">Our Electronics Services</h2>
      <div class="grid md:grid-cols-2 gap-8">
        <div>
          <h3 class="text-lg font-semibold mb-4">Custom Design</h3>
          <p class="text-gray-600 mb-4">
            We offer custom electronic design services tailored to your specific requirements. Our team of experienced engineers can help you develop prototypes and scale to production.
          </p>
          <ul class="space-y-2">
            <li class="flex items-center space-x-2">
              <Icon name="i-heroicons-check-circle" class="w-4 h-4 text-green-500" />
              <span>Circuit design and simulation</span>
            </li>
            <li class="flex items-center space-x-2">
              <Icon name="i-heroicons-check-circle" class="w-4 h-4 text-green-500" />
              <span>PCB layout and prototyping</span>
            </li>
            <li class="flex items-center space-x-2">
              <Icon name="i-heroicons-check-circle" class="w-4 h-4 text-green-500" />
              <span>Firmware development</span>
            </li>
          </ul>
        </div>
        <div>
          <h3 class="text-lg font-semibold mb-4">Supply Chain Solutions</h3>
          <p class="text-gray-600 mb-4">
            Comprehensive supply chain management for electronic components with quality assurance and timely delivery.
          </p>
          <ul class="space-y-2">
            <li class="flex items-center space-x-2">
              <Icon name="i-heroicons-check-circle" class="w-4 h-4 text-green-500" />
              <span>Global sourcing network</span>
            </li>
            <li class="flex items-center space-x-2">
              <Icon name="i-heroicons-check-circle" class="w-4 h-4 text-green-500" />
              <span>Quality control and testing</span>
            </li>
            <li class="flex items-center space-x-2">
              <Icon name="i-heroicons-check-circle" class="w-4 h-4 text-green-500" />
              <span>Inventory management</span>
            </li>
          </ul>
        </div>
      </div>
    </section>

    <section class="text-center py-12">
      <h2 class="text-2xl font-semibold mb-6">Quality Assurance</h2>
      <p class="text-gray-600 mb-8 max-w-3xl mx-auto">
        All our electronic components undergo rigorous testing and quality control processes to ensure they meet international standards and customer specifications.
      </p>
      <UButton to="/contact" size="lg" color="primary">
        Get Quote for Electronic Components
      </UButton>
    </section>
  </div>
</template>

<script setup>
useHead({
  title: 'Electronics - Agri-Management',
  meta: [
    { name: 'description', content: 'Cutting-edge electronic components and solutions for modern industries' }
  ]
})
</script>
