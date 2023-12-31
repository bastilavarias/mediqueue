<template>
  <div>
    <div class="container q-mb-xl q-pa-sm">
      <div class="row q-col-gutter-md">
        <div class="col-12 col-md-6">
          <div>
            <h5 class="text-bold">WHAT IS MEDIQUEUE?</h5>
            <p class="text-body1 q-pl-md">
              MediQueue is a digital scheduling website made to streamline
              patient experiences in booking their appointment in clinics. Aside
              from allowing patients to book their clinical appointments online,
              MediQueue can also show the patients' queueing numbers to check
              their current standing for the day they booked a schedule to avoid
              long waiting lines and save patients' time.
            </p>
          </div>
        </div>

        <div class="col-12 col-md-6">
          <div>
            <h5 class="text-bold">HISTORY OF MEDIQUEUE?</h5>
            <p class="text-body1 q-pl-md">
              MediQueue is a website created by the students of Valenzuela City
              School of Mathematics and Science in line with their research
              study entitled "MediQueue: Streamlining Patient Care in Private
              Health Clinics Through a Digital Scheduling Website." The website
              was officially launched in January 2024. Its features respond to
              the needs of addressing the research objectives of the study.
            </p>
          </div>
        </div>
      </div>
    </div>
    <div class="bg-primary q-pa-sm" style="padding: 5rem 0">
      <div class="container text-white">
        <div class="row q-col-gutter">
          <template v-for="(feature, index) in features" :key="index">
            <div class="col-12 col-md-3 q-pa-md">
              <div class="text-center">
                <q-icon
                  :name="feature.icon"
                  size="5rem"
                  class="q-mb-md"
                ></q-icon>
                <div class="text-center text-h6 q-mb-md text-weight-bold">
                  {{ feature.title }}
                </div>
                <div class="text-center text-subtitle1 q-mb-none">
                  {{ feature.description }}
                </div>
              </div>
            </div>
          </template>
        </div>
      </div>
    </div>
    <div class="container q-mb-xl q-pa-sm">
      <div class="row q-col-gutter-md">
        <div class="col-12 col-md-6">
          <div>
            <h6>Proponents</h6>
            <div class="row q-col-gutter">
              <template v-for="(proponent, index) in proponents" :key="index">
                <div class="col-6 col-md-3">
                  <div>
                    <div class="text-center">
                      <q-avatar class="q-mb-sm" size="3rem">
                        <img :src="proponent.image" />
                      </q-avatar>
                      <div class="text-center text-weight-medium">
                        {{ proponent.name }}
                      </div>
                    </div>
                  </div>
                </div>
              </template>
            </div>
          </div>
        </div>
        <div class="col-12 col-md-6">
          <div>
            <h6>Developer</h6>
            <div class="flex justify-center">
              <div class="row q-col-gutter-sm">
                <div class="col-12 col-md-6">
                  <div>
                    <q-avatar size="9rem" class="q-mb-sm">
                      <img :src="MeImage" />
                    </q-avatar>
                  </div>
                </div>
                <div class="col-12 col-md-6">
                  <div>
                    <div class="text-weight-bold">
                      Lavarias, Sebastian Curtis T.
                    </div>
                    <div class="text-weight-medium">
                      Full-stack Web Developer
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import { defineComponent } from 'vue';

export default defineComponent({
  name: 'AboutUsWindow',
});
</script>

<script setup>
import ArchieImage from '../assets/proponents/archie.jpg';
import AshleeImage from '../assets/proponents/ashlee.png';
import DorynImage from '../assets/proponents/doryn.jpeg';
import MichaelaImage from '../assets/proponents/michaela.jpeg';
import SofiaImage from '../assets/proponents/sofia.jpeg';
import IsaacImage from 'assets/proponents/isaac.jpg';
import MeImage from 'assets/me.jpg';

const features = [
  {
    icon: 'event',
    title: 'Effortless Scheduling',
    description:
      'Take control of your time with our intuitive appointment system. Your schedule, your way.',
  },
  {
    icon: 'update',
    title: 'Stay on Top',
    description:
      'Our Schedule Tracker keeps you in the loop, ensuring you never miss a beat. Real-time updates, always at your fingertips.',
  },
  {
    icon: 'account_circle',
    title: 'Manage with Ease',
    description:
      'Simplify your life with our comprehensive Account Management tools. Your details, your preferences—perfectly organized.',
  },
  {
    icon: 'mobile_friendly',
    title: 'Go Where You Go',
    description:
      "Experience ultimate flexibility with our mobile-friendly design. Access anytime, anywhere, because your world doesn't stand still.",
  },
];

const proponents = [
  {
    image: AshleeImage,
    name: 'Armas, Ashlee B.',
  },
  {
    image: SofiaImage,
    name: 'Bartolo, Sofia P.',
  },
  {
    image: DorynImage,
    name: 'David, Doryn Maurice C.',
  },
  {
    image: MichaelaImage,
    name: 'Domingo, Micaela Denise G.',
  },
  {
    image: ArchieImage,
    name: 'Ferrera, Archie B.',
  },
  {
    image: IsaacImage,
    name: 'Melgar, Isaac Gregory P.',
  },
];
</script>
