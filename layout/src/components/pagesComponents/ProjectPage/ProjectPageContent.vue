<template>
  <section class="project center">
    <ProjectPageCategories @activCategories="activCategories" />
    <ProjectPageProjects :projects="projects" />
    <div class="project__count-page">
      <div class="project__count-page-wrap">
        <a href="#" class="project__count-page-number">
          <p class="project__count-page-number-text">01</p>
        </a>
        <a href="#" class="project__count-page-number">
          <p class="project__count-page-number-text">02</p>
        </a>
        <a href="#" class="project__count-page-number">
          <p class="project__count-page-number-text">03</p>
        </a>
        <a href="#">
          <svg class="project__count-page-svg" xmlns="http://www.w3.org/2000/svg" width="53" height="52"
            viewBox="0 0 53 52" fill="none">
            <circle cx="26.5" cy="26" r="25.5" stroke="#CDA274" />
            <path d="M23.5571 32L29.5 25.3143L23.5571 18.6286" stroke="#292F36" stroke-width="2" stroke-linecap="round"
              stroke-linejoin="round" />
          </svg>
        </a>
      </div>
    </div>
  </section>
</template>

<script>
import ProjectPageCategories from './ProjectPageCategories.vue'
import ProjectPageProjects from './ProjectPageProjects.vue'
export default {
  components: {
    ProjectPageCategories,
    ProjectPageProjects
  },
  name: 'ProjectPageContent',

  data () {
    return {
      projects: [],
      projectsOne: [
        {
          id: 1,
          image: 'project__item_1.jpg',
          title: 'Минималистичная спальня',
          text: 'Декор / Планировка'
        },
        {
          id: 2,
          image: 'project__item_3.jpg',
          title: 'Классическая спальня',
          text: 'Декор / Планировка'
        },
        {
          id: 3,
          image: 'project__item_5.jpg',
          title: 'Минималистичный прикроватный столик',
          text: 'Декор / Планировка'
        },
        {
          id: 4,
          image: 'project__item_7.jpg',
          title: 'Современная спальня',
          text: 'Декор / Планировка'
        },
        {
          id: 5,
          image: 'project__item_2.jpg',
          title: 'Минималистичная спальня',
          text: 'Декор / Планировка'
        },
        {
          id: 6,
          image: 'project__item_4.jpg',
          title: 'Современная спальня',
          text: 'Декор / Планировка'
        },
        {
          id: 7,
          image: 'project__item_6.jpg',
          title: 'Столы и столики',
          text: 'Декор / Планировка'
        },
        {
          id: 8,
          image: 'project__item_8.jpg',
          title: 'Современная спальня',
          text: 'Декор / Планировка'
        }
      ],
      projectsNew: [
        {
          id: 1,
          image: 'project__item_2.jpg',
          title: 'Минималистичная спальня',
          text: 'Декор / Планировка'
        },
        {
          id: 2,
          image: 'project__item_4.jpg',
          title: 'Современная спальня',
          text: 'Декор / Планировка'
        },
        {
          id: 3,
          image: 'project__item_6.jpg',
          title: 'Столы и столики',
          text: 'Декор / Планировка'
        },
        {
          id: 4,
          image: 'project__item_8.jpg',
          title: 'Современная спальня',
          text: 'Декор / Планировка'
        },
        {
          id: 5,
          image: 'project__item_1.jpg',
          title: 'Минималистичная спальня',
          text: 'Декор / Планировка'
        },
        {
          id: 6,
          image: 'project__item_3.jpg',
          title: 'Классическая спальня',
          text: 'Decor / Artchitecture'
        },
        {
          id: 7,
          image: 'project__item_5.jpg',
          title: 'Минималистичный прикроватный столик',
          text: 'Декор / Планировка'
        },
        {
          id: 8,
          image: 'project__item_7.jpg',
          title: 'Современная спальня',
          text: 'Декор / Планировка'
        }
      ],
      projectsTwo: [
        {
          id: 1,
          image: 'project__item_5.jpg',
          title: 'Минималистичный прикроватный столик',
          text: 'Декор / Планировка'
        },
        {
          id: 2,
          image: 'project__item_2.jpg',
          title: 'Минималистичная спальня',
          text: 'Декор / Планировка'
        },
        {
          id: 3,
          image: 'project__item_3.jpg',
          title: 'Классическая спальня',
          text: 'Декор / Планировка'
        },
        {
          id: 4,
          image: 'project__item_4.jpg',
          title: 'Современная спальня',
          text: 'Декор / Планировка'
        },
        {
          id: 5,
          image: 'project__item_1.jpg',
          title: 'Minimal Bedroom',
          text: 'Декор / Планировка'
        },
        {
          id: 6,
          image: 'project__item_6.jpg',
          title: 'Столы и столики',
          text: 'Декор / Планировка'
        },
        {
          id: 7,
          image: 'project__item_7.jpg',
          title: 'Современная спальня',
          text: 'Декор / Планировка'
        },
        {
          id: 8,
          image: 'project__item_8.jpg',
          title: 'Современная спальня',
          text: 'Декор / Планировка'
        }
      ]
    }
  },

  created () {
    this.projects = this.projectsOne
  },

  methods: {
    activCategories (data) {
      switch (data.id) {
        case 1:
          this.projects = this.projectsTwo
          break
        case 2:
          this.projects = this.projectsOne
          break
        case 3:
          this.projects = this.projectsNew
          break
        case 4:
          this.projects = this.projectsNew
          break
      }
    }
  }
}
</script>

<style lang="scss" scoped>
@import "../../../scss/vars";

.project {
  &__count-page {
    margin-top: 51px;
    margin-bottom: 200px;
    display: flex;
    justify-content: center;

    &-wrap {
      display: flex;
      gap: 20px;
    }

    &-number {
      display: flex;
      justify-content: center;
      align-items: center;
      flex-wrap: nowrap;
      border: 1px #cda274 solid;
      width: 52px;
      height: 52px;
      border-radius: 52px;

      &-text {
        color: #292f36;
        font-family: $familyText;
        font-size: 16px;
        font-style: normal;
        font-weight: $font-500;
        line-height: 150%;
        text-transform: capitalize;
      }

      &:hover {
        background: #f4f0ec;
        border: none;
        width: 54px;
        height: 54px;
      }
    }

    &-svg:hover {
      fill: #f4f0ec;

      & circle {
        stroke: none;
      }
    }
  }
}
</style>
