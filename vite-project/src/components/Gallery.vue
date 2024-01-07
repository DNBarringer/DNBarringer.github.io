<template>
    <VRow>
        <!-- <VCol v-for="(photo, index) in photos" :key="index" cols="12" sm="6" md="4" lg="3">
            <VCard>
                <VImg :src="photo" alt="Photo" aspect-ratio="1" cover>
                    <template v-slot:placeholder>
                        <div class="d-flex align-center justify-center fill-height">
                            <VProgressCircular
                            color="grey-lighten-4"
                            indeterminate
                            ></VProgressCircular>
                        </div>
                </template>
                </VImg>
            </VCard>
        </VCol> -->
    </VRow>
  </template>
  
  <!-- <script lang="ts">
  import { defineComponent } from 'vue';
  
  interface ImagePathFunction {
    default: string;
  }
  
  export default defineComponent({
    data() {
      return {
        photos: [] as string[]
      };
    },
    async mounted() {
      try {
        console.log("FETCHING");
        const context = import.meta.glob('../assets/photos/sony/**/*.(png|jpg|svg)');
        const images = Object.values(context);

        const photoOrder = [
          'DSC01317.jpg',
        ];

        for (const orderedPhoto of photoOrder) {
          for (const imagePromise of images) {
            const imagePath = await (imagePromise as () => Promise<ImagePathFunction>)();
            const filename = imagePath.default.split('/').pop() || ''; // Extract the filename from the path

            if (filename === orderedPhoto) {
              this.photos.push(imagePath.default);
              break;
            }
          }
        }
      } catch (error) {
        console.error('Error fetching images:', error);
      } finally {
        console.log('Photos:', this.photos); // Log fetched photos for debugging
      }
    }
  });
  </script>
   -->