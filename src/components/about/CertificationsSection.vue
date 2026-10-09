<script setup>
import { ShieldCheck, Award, FileCheck, CheckCircle } from 'lucide-vue-next'
import companyData from '@/data/company.json'
import SectionTitle from '@/components/ui/SectionTitle.vue'

const certifications = companyData.certifications
</script>

<template>
  <section class="py-20 bg-slate-50 border-t border-slate-200">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      
      <!-- Section Header -->
      <SectionTitle
        badge="Legalitas & Sertifikasi Resmi"
        title="Standar Kepatuhan Regulasi & Manajemen Mutu"
        description="Seluruh operasional rekayasa dan eksekusi konstruksi kami telah terakreditasi dan memiliki izin resmi berskala nasional."
        align="center"
      />

      <!-- Certifications Cards Grid -->
      <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-6 mt-12">
        <div
          v-for="(cert, idx) in certifications"
          :key="idx"
          class="bg-white rounded-2xl p-7 border border-slate-200/80 hover:border-amber-400 hover:shadow-xl transition-all duration-300 flex flex-col justify-between group"
        >
          <div>
            <div class="w-12 h-12 rounded-xl bg-amber-50 group-hover:bg-amber-500 text-amber-600 group-hover:text-slate-950 flex items-center justify-center font-bold mb-6 transition-colors shadow-sm">
              <ShieldCheck class="w-6 h-6" />
            </div>

            <h3 class="text-base font-bold text-slate-900 group-hover:text-amber-600 transition-colors mb-2 leading-snug">
              {{ cert.name }}
            </h3>

            <p class="text-xs text-slate-500 font-medium">
              Penerbit: <span class="text-slate-700 font-semibold">{{ cert.issuer }}</span>
            </p>
          </div>

          <div class="mt-6 pt-4 border-t border-slate-100 flex items-center justify-between text-xs text-emerald-600 font-bold">
            <span class="flex items-center gap-1.5">
              <CheckCircle class="w-4 h-4 text-emerald-500" />
              Status Aktif
            </span>
            <span class="text-slate-400 font-mono text-[10px]">VERIFIED</span>
          </div>
        </div>
      </div>

    </div>
  </section>
</template>
