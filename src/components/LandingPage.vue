<script setup>

</script>

<template>
    <v-container max-width="100%">
        <v-row>
            <v-col>
                <v-carousel cycle hide-delimiters>
                    <v-carousel-item src="/images/carousel1.jpg"cover></v-carousel-item>
                     <v-carousel-item src="/images/carousel2.jpg"cover></v-carousel-item>
                      <v-carousel-item src="/images/carousel3.jpg"cover></v-carousel-item>
                       <v-carousel-item src="/images/carousel4.jpg"cover></v-carousel-item>
                </v-carousel>
            </v-col>
        </v-row>
    </v-container>

    <!-- About Us -->
    <v-container max-width="100%">
        <v-row>
            <v-col>
                <v-card align="center">
                <v-card-title>Welcome to the Luwa Hospital</v-card-title>
                <v-card-text class="text-body-large">Your health. Your life. Our commitment. At Luwa Hospital, we bring together compassionate care, modern healthcare, and a team that truly puts you first. Whether it’s a routine check-up, emergency care, or specialized treatment, we’re here to make every step of your healthcare journey feel safer, simpler, and better.</v-card-text>
                <v-card-text class="text-body-large">Because when you feel your best, you can live your best.</v-card-text>
                </v-card>
            </v-col>
        </v-row>
    </v-container>

    <!-- clinics -->
     <v-container max-width="100%">
        <v-row>
            <v-col md="3">
                <v-card width="300px"color="primary">
                    <v-img src="/images2/clinic7.jpg"cover height="200px"></v-img>
                    <v-card-title>Laboratory services</v-card-title>
                    <v-card-text>some text about the lab</v-card-text>
                    <v-btn class="ma-4">Learn More</v-btn>
                </v-card>
            </v-col>

            <v-col md="3">
                <v-card width="300px"color="primary">
                    <v-img src="/images2/clinic8.jpg"cover height="200px"></v-img>
                    <v-card-title>Maternity services</v-card-title>
                    <v-card-text>some text about the lab</v-card-text>
                    <v-btn class="ma-4">Learn More</v-btn>
                </v-card>
            </v-col>

            <v-col md="3">
                <v-card width="300px"color="primary">
                    <v-img src="/images2/clinic10.jpg"cover height="200px"></v-img>
                    <v-card-title>Physiotherapy Services</v-card-title>
                    <v-card-text>some text about the lab</v-card-text>
                    <v-btn class="ma-4">Learn More</v-btn>
                </v-card>
            </v-col>

            <v-col md="3">
                <v-card width="300px"color="primary">
                    <v-img src="/images2/clinic9.jpg"cover height="200px"></v-img>
                    <v-card-title>Dental services</v-card-title>
                    <v-card-text>some text about the lab</v-card-text>
                    <v-btn class="ma-4">Learn More</v-btn>
                </v-card>
            </v-col>
        </v-row>
     </v-container>

     <!-- Footer -->
      <v-container max-width="100%" class="mt-6 bg-secondary">
        <v-row> 
            <v-col md="4">
                <v-card height="300px"color="secondary" flat>
                    <v-card-title>subscribe to our mailing list</v-card-title>
                    <v-card-text>Get the latest news, health tips, and  hopital updates delivered to your inbox</v-card-text>
                    <v-text-field v-model="inputvalue" label="Email address"outlined class="ma-4">
                        <template v-slot:append-inner>
                        <v-btn color="primary">subscribe </v-btn>
                        </template>
                    </v-text-field>
                    <div class="text-center mb-4">
                        <p>Follow us on:</p>
                        <v-icon icon="mdi-instagram"></v-icon>
                        <v-icon icon="mdi-twitter"></v-icon>
                        <v-icon icon="mdi-facebook"></v-icon>

                    </div>
                </v-card>
            </v-col>
            <v-col md="4">
                <v-card height="300px"color="secondary"flat>
                    <v-card-title>Contact Information</v-card-title>
                    <v-card-text>
                        <p>
                            <v-icon icon="mdi-map-marker-radius-outline"></v-icon>
                            The Luwa Hospital
                        </p>
                        <p>132,main street, Nairobi</P>
                            <p>2547132589213</p>
                        <P>
                            <v-icon icon="mdi-email-outline"></v-icon>
                            info@theluwahospital.commitment
                        </p>
                    </v-card-text>
                </v-card>
            </v-col>
            <v-col>
                <v-card height="300px"color="secondary"flat>
                    <v-card-title>Quick Links</v-card-title>
                    <v-card-text>About Us</v-card-text>
                    <v-card-text>Clinics</v-card-text>
                    <v-card-text>Find a Doctor</v-card-text>
                    <v-card-text>News and Events</v-card-text>
                </v-card>
            </v-col>
        </v-row>
    </v-container>
    </template>