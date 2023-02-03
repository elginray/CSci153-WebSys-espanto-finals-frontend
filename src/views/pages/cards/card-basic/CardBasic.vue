<script setup>
import avatar1 from '@/assets/images/avatars/avatar-1.png'
import avatar2 from '@/assets/images/avatars/avatar-2.png'
import avatar3 from '@/assets/images/avatars/avatar-3.png'
import avatar4 from '@/assets/images/avatars/avatar-4.png'
import eCommerce2 from '@/assets/images/eCommerce/2.png'
import pages1 from '@/assets/images/pages/1.png'
import pages2 from '@/assets/images/pages/2.png'
import pages3 from '@/assets/images/pages/3.png'
import pages5 from '@/assets/images/pages/5.jpg'
import pages6 from '@/assets/images/pages/6.jpg'

const avatars = [
  avatar1,
  avatar2,
  avatar3,
  avatar4,
]
const isCardDetailsVisible = ref(false)
</script>

<template>
  <VRow>
    <!-- 👉 Influencing The Influencer -->
    <VCol
      cols="12"
      sm="6"
      md="4"
    >
      <VCard>
        <VImg
          :src="pages1"
          cover
        />

        <VCardItem>
          <VCardTitle>Canigao Island</VCardTitle>
        </VCardItem>

        <VCardText>
          <justify> <hr> <br>🏝️ Canigao Island is 🏝️ uninhabited, featuring a lighthouse as its only significant man-made structure. <br>
          <b>Features: </b> <br>
          The beaches have white sand, with tropical sea creatures and extensive coral reef in the surrounding waters. The climate is tropical and similar to that found in other areas of the 🇵🇭 Philippine islands.
        </justify>
        </VCardText>
      </VCard>
    </VCol>



    <!-- 👉 Popular Uses Of The Internet -->
    <VCol
      cols="12"
      md="4"
      sm="6"
    >
      <VCard>
        <VImg :src="pages3" />

        <VCardItem>
          <VCardTitle>Kalanggaman Island</VCardTitle>
        </VCardItem>

        <VCardText>
          Kalanggaman Island: A tropical paradise of crystal clear waters, white sands, and vibrant coral reefs.
        </VCardText>

        <VCardActions>
          <VBtn @click="isCardDetailsVisible = !isCardDetailsVisible">
            Details
          </VBtn>

          <VSpacer />

          <VBtn
            icon
            size="small"
            @click="isCardDetailsVisible = !isCardDetailsVisible"
          >
            <VIcon :icon="isCardDetailsVisible ? 'mdi-chevron-up' : 'mdi-chevron-down'" />
          </VBtn>
        </VCardActions>

        <VExpandTransition>
          <div v-show="isCardDetailsVisible">
            <VDivider />
            <VCardText>
              🌴Escape to the breathtaking beauty of Kalanggaman Island! 🏝️This remote paradise boasts crystal clear waters, powdery white sands, and a vibrant coral reef ecosystem. 🌞Soak up the tropical sun and go on island adventures you'll never forget. Book your trip now and discover why Kalanggaman Island is a must-visit destination in the Philippines!🌴
            </VCardText>
          </div>
        </VExpandTransition>
      </VCard>
    </VCol>

        <!-- 👉 Robert Meyer -->
        <VCol
      cols="12"
      sm="6"
      md="4"
    >
      <VCard>
        <VImg :src="pages2" />

        <VCardText class="position-relative">
          <!-- User Avatar -->
          <VAvatar
            size="75"
            class="avatar-center"
            :image="avatar1"
          />

          <!-- Title, Subtitle & Action Button -->
          <div class="d-flex justify-space-between flex-wrap pt-8">
            <div class="me-2 mb-2">
              <VCardTitle class="pa-0">
                Jake Albero
              </VCardTitle>
              <VCardSubtitle class="text-caption pa-0">
                Gabas, Baybay
              </VCardSubtitle>
            </div>
            <VBtn>send request</VBtn>
          </div>

          <!--  Mutual Friends -->
          <div class="d-flex justify-space-between align-center mt-8">
            <span class="font-weight-medium">18 mutual friends</span>

            <div class="v-avatar-group">
              <VAvatar
                v-for="avatar in avatars"
                :key="avatar"
                :image="avatar"
                size="45"
              />
            </div>
          </div>
        </VCardText>
      </VCard>
    </VCol>

    <!-- 👉 Apple iPhone 11 Pro -->
    <VCol
      sm="6"
      cols="12"
    >
      <VCard>
        <div class="d-flex justify-space-between flex-wrap flex-md-nowrap flex-column flex-md-row">
          <div class="ma-auto pa-5">
            <VImg
              width="137"
              :src="eCommerce2"
            />
          </div>

          <VDivider :vertical="$vuetify.display.mdAndUp" />

          <div>
            <VCardItem>
              <VCardTitle>Apple iPhone 11 Pro</VCardTitle>
            </VCardItem>

            <VCardText>
              Apple iPhone 11 Pro smartphone. Announced Sep 2019. Features 5.8″ display Apple A13 Bionic
            </VCardText>

            <VCardText class="text-subtitle-1">
              <span>Price :</span> <span class="font-weight-bold">$899</span>
            </VCardText>

            <VCardActions class="justify-space-between">
              <VBtn>
                <VIcon icon="mdi-cart-plus" />
                <span class="ms-2">Add to cart</span>
              </VBtn>

              <VBtn
                color="secondary"
                icon="mdi-share-variant-outline"
              />
            </VCardActions>
          </div>
        </div>
      </VCard>
    </VCol>

    <!-- 👉 Stump town Roasters. -->
    <VCol
      sm="6"
      cols="12"
    >
      <VCard>
        <div class="d-flex flex-column-reverse flex-md-row">
          <div>
            <VCardItem>
              <VCardTitle>Stumptown Roasters</VCardTitle>
            </VCardItem>

            <VCardText class="d-flex align-center flex-wrap body-1">
              <VRating
                :model-value="5"
                readonly
                class="me-3"
                density="compact"
              />
              <span>5 Star | 98 reviews</span>
            </VCardText>

            <VCardText>
              Before there was a United States of America, there were coffee houses, because how are you supposed to build.
            </VCardText>

            <VCardActions>
              <VBtn>Location</VBtn>
              <VBtn>Reviews</VBtn>
            </VCardActions>
          </div>

          <div class="ma-auto pa-5">
            <VImg
              :width="176"
              :src="pages5"
              class="rounded"
            />
          </div>
        </div>
      </VCard>
    </VCol>




    <!-- 👉 Kalanggaman Island package -->
    <VCol
      md="6"
      lg="8"
      cols="12"
    >
      <VCard>
        <VRow no-gutters>
          <VCol
            cols="12"
            sm="8"
            md="12"
            lg="7"
            order="2"
            order-lg="1"
          >
            <VCardItem>
              <VCardTitle>Kalanggaman Island</VCardTitle>
            </VCardItem>

            <VCardText>
              🏝️Escape to the tropical paradise of Kalanggaman Island this holiday season at a reduced price! 💰🌊Savor crystal clear waters, pristine white sands, and a vibrant coral reef ecosystem. 🌞Ideal for relaxation and adventure, this remote island is the perfect escape from the hustle and bustle. Book now for an unforgettable experience filled with sun, sea, and serenity at a fraction of the cost!🌴
            </VCardText>

            <VCardText>
              <VDivider />
            </VCardText>

            <VCardText class="d-flex justify-center">
              <div class="me-auto pe-4">
                <p class="d-flex align-center mb-6">
                  <VIcon
                    color="primary"
                    icon="mdi-lock-open-outline"
                  />
                  <span class="ms-3">Full Access</span>
                </p>

                <p class="d-flex align-center mb-0">
                  <VIcon
                    color="primary"
                    icon="mdi-account-outline"
                  />
                  <span class="ms-3">10 members</span>
                </p>
              </div>

              <VDivider
                v-if="$vuetify.display.smAndUp"
                vertical
                inset
              />

              <div class="ms-auto ps-4">
                <p class="d-flex align-center mb-6">
                  <VIcon
                    color="primary"
                    icon="mdi-star-outline"
                  />
                  <span class="ms-3">Free Freebies</span>
                </p>

                <p class="d-flex align-center mb-0">
                  <VIcon
                    color="primary"
                    icon="mdi-trending-up"
                  />
                  <span class="ms-3">Excellent Staff and crew</span>
                </p>
              </div>
            </VCardText>
          </VCol>

          <VCol
            cols="12"
            sm="4"
            md="12"
            lg="5"
            order="1"
            order-lg="2"
            class="member-pricing-bg text-center"
          >
            <div class="membership-pricing d-flex flex-column align-center py-14 h-100 justify-center">
              <p class="mb-5">
                <sub class="text-h5">$</sub>
                <sup class="text-h2 font-weight-medium">799</sup>
                <sub class="text-h5">USD</sub>
              </p>

              <p class="text-sm">
                Holiday <br> Island Package
              </p>

              <VBtn class="mt-8">
                Contact Now
              </VBtn>
            </div>
          </VCol>
        </VRow>
      </VCard>
    </VCol>

    <!-- 👉 Influencing The Influencer -->
    <VCol
      cols="12"
      lg="4"
      md="6"
    >
      <VCard title="Influencing The Influencer">
        <VCardText>
          Computers have become ubiquitous in almost every facet of our lives. At work, desk jockeys spend hours in front of their desktops, while delivery people scan bar codes with handhelds and workers in the field stay in touch.
        </VCardText>

        <VCardText>
          If you're in the market for new desktops, notebooks, or PDAs, there are a myriad of choices. Here's a rundown of some of the best systems available.
        </VCardText>

        <VCardActions>
          <VBtn>Read More</VBtn>
        </VCardActions>
      </VCard>
    </VCol>

    <!-- 👉 The Best Answers -->
    <VCol
      cols="12"
      lg="4"
      md="6"
    >
      <VCard title="The Best Answers">
        <VCardText class="d-flex align-center flex-wrap">
          <VRating
            :model-value="5"
            readonly
            density="compact"
            class="me-3"
          />
          <span class="text-subtitle-2">5 Star | 98 reviews</span>
        </VCardText>

        <VCardText>
          If you are looking for a new way to promote your business that won't cost you more money, maybe printing is one of the options you won't resist.
        </VCardText>

        <VCardText>
          become fast, easy and simple. If you want your promotional material to be an eye-catching
        </VCardText>

        <VCardActions>
          <VBtn>Location</VBtn>
          <VBtn>Reviews</VBtn>
        </VCardActions>
      </VCard>
    </VCol>

    <!-- 👉 Support -->
    <VCol
      cols="12"
      md="6"
      lg="4"
    >
      <VCard class="text-center">
        <VCardText class="d-flex flex-column justify-center align-center">
          <VAvatar
            color="primary"
            variant="tonal"
            size="50"
            class="mb-4"
          >
            <VIcon
              size="2rem"
              icon="mdi-help-circle-outline"
            />
          </VAvatar>

          <h6 class="text-h6">
            Support
          </h6>
        </VCardText>

        <VCardText>
          <p>
            According to us blisters are a very common thing and we come across them very often in our daily lives. It is a very common occurrence like cold or fever depending upon your lifestyle.
          </p>
        </VCardText>

        <VCardActions class="justify-center">
          <VBtn variant="elevated">
            Contact Now
          </VBtn>
        </VCardActions>
      </VCard>
    </VCol>
  </VRow>
</template>

<style lang="scss" scoped>
.avatar-center {
  position: absolute;
  border: 3px solid rgb(var(--v-theme-surface));
  inset-block-start: -2rem;
  inset-inline-start: 1rem;
}

// // membership pricing
// .member-pricing-bg {
//   position: relative;
//   background-color: rgba(var(--v-theme-on-surface), var(--v-hover-opacity));
// }

// .membership-pricing {
//   sup {
//     inset-block-start: 9px;
//   }
// }
</style>
