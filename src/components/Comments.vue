<template>
   <v-container>
        <v-row no-gutters>
            <v-col cols="12" class="pa-2 ma-2">
                <v-card class="pa-3">
                    <span class="user-heading">{{user.FullName}}</span>
                    <div class="user-subheading">
                        <span>About Me:</span>
                    </div>
                    <div>
                        <span class="user-subheading">Full Name:</span><span> {{user.FullName}}</span>
                    </div>
                    <div>
                        <span class="user-subheading">User Name:</span><span> {{user.UserName}}</span>
                    </div>
                    <div>
                        <span class="user-subheading">Email:</span><span> {{user.Email}}</span>
                    </div>
                    <div>
                        <span class="user-subheading">Website:</span><span> {{user.Website}}</span>
                    </div>
                </v-card>
            </v-col>
        </v-row>
        <div v-for="post in user.Posts" :key="post.id">
            <v-row no-gutters>
                <v-col cols="12" class="pa-2 ma-2">
                    <Post :post="post"></Post>
                </v-col>
            </v-row>
        </div>

    </v-container>

</template>

<script>
import Post from './Post';

export default {
    name: 'Comments',
  components: {
    Post
  },
  data: () => ({
      user: {
          FullName: "Krystal Rae Randall",
          UserName: "Rae",
          Email: "krystal.randall@gmail.com",
          Website: "www.krystal-chandelier.com", 
          Posts: [
              {
                  id: 1,
                  title: "lets get this going",
                  text: "i hope this works",
                  comments: [{
                      author: "me",
                      comment: "lalala"
                  },{
                      author: "greg",
                      comment: "sup sup"
                  }]

          },{
              id: 2,
              title: "are you going to work",
                  text: "yes no yes no",
                  comments: [{
                      author: "me",
                      comment: "hahahaha"
                  },{
                      author: "xavier",
                      comment: "lskfdhlakhf"
                  }]
          },{
              id: 3,
              title: ";ODFJ;sdjg",
                  text: "wg;jsadl;kg",
                  comments: [{
                      author: "dgdfg",
                      comment: "hfghs"
                  },{
                      author: "fhdh",
                      comment: "fdgdh"
                  }]
          }]         
      }
  })
}

</script>

<style>
.user-heading{
    display: block;
    text-align: center;
    font-size: 20px;
}

.user-subheading{
    font-family:Arial, Helvetica, sans-serif;
    font-size: 16px;
    font-weight: bold;
}

.v-content{
    background-color:blueviolet;
}

</style>
