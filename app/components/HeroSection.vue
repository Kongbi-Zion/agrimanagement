<template>
  <section class="relative rounded-br-[2.5rem] md:rounded-br-[8.5rem] min-h-[calc(100vh-130px)] md:min-h-[calc(100vh-100px)] bg-cover bg-center bg-no-repeat bg-[url('/hero-bg.jpg')]">
    <div class="absolute inset-0 bg-black/50 rounded-br-[2.5rem] md:rounded-br-[8.5rem]"></div>
    
    <AppHeader class="relative z-10" />
    
    <div class="relative z-10 flex items-center min-h-[calc(100vh-130px)] md:min-h-[calc(100vh-100px)]">
      <div class="w-full max-w-7xl mx-auto max-md:px-4">
        <div class="grid lg:grid-cols-2 gap-8 lg:gap-12">
          <div class="text-white space-y-6">
            <h1 class="text-3xl lg:text-5xl font-semibold leading-tight">
              Agri-Management: Export-Import Cameroon's Finest Cocoa & Coffee
            </h1>
            <p class="text-sm md:text-lg font-light leading-relaxed opacity-90">
              We specialize in the export-import of high-quality coffee, cocoa beans, and cocoa residues, including cocoa butter, cocoa mass, cocoa powder, and cocoa shells. All sustainably sourced and expertly processed for international partners.
            </p>
            <div class="pt-8 flex max-lg:justify-center">
              <NuxtLink 
                to="/about"
                class="inline-flex items-center px-5 py-4 text-[14px] font-sm bg-primary text-white rounded-lg hover:bg-primary/90 transition-colors group"
              >
                Learn More
                <Icon name="i-heroicons-arrow-right" class="w-4 h-4 ml-1 transition-transform duration-300 group-hover:translate-x-1" />
              </NuxtLink>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>
