<template>
  <div>
    <div v-for="(user, index) in users" :key="user.id" class="user-card">
      <div>
        <span>
          {{ index + 1 }}
        </span>

        <img :src="user.img" alt="user" />
        <span class="username">{{ user.name }}</span>
      </div>
      <div>
        + {{ user.pointsGained }}
      </div>
    </div>

      <div class="lead-footer">
      <p>
        This week you're ranked 5815 out of 10720 students for points earned!
      </p>
    </div>
  </div>
</template>

<script>
export default {
  name: "Card",
  data() {
    return {
      users: [
        {
          id: 1,
          img: "https://campmessenger.com/wp-content/uploads/2019/03/user.png",
          name: "Ed Wheeler",
          pointsGained: 74,
        },
        {
          id: 2,
          img:
            "https://images.pexels.com/photos/3648118/pexels-photo-3648118.jpeg",
          name: "Mark Thompson",
          pointsGained: 47,
        },
        {
          id: 3,
          img: "https://campmessenger.com/wp-content/uploads/2019/03/user.png",
          name: "Dwayne Wright",
          pointsGained: 44,
        },
        {
          id: 4,
          img: "https://campmessenger.com/wp-content/uploads/2019/03/user.png",
          name: "Denim Mazuki",
          pointsGained: 44,
        },
        {
          id: 5,
          img:
            "https://images.pexels.com/photos/1002008/pexels-photo-1002008.jpeg",
          name: "Christian Eriebach",
          pointsGained: 44,
        },
        {
          id: 6,
          img: "https://campmessenger.com/wp-content/uploads/2019/03/user.png",
          name: "Jordimartinoy",
          pointsGained: 43,
        },
        {
          id: 7,
          img:
            "https://images.pexels.com/photos/4652580/pexels-photo-4652580.jpeg",
          name: "Dev Conmio",
          pointsGained: 43,
        },
        {
          id: 8,
          img:
            "https://images.pexels.com/photos/4791470/pexels-photo-4791470.jpeg",
          name: "Robin mimeault",
          pointsGained: 36,
        },
        {
          id: 9,
          img:
            "https://images.pexels.com/photos/4754623/pexels-photo-4754623.jpeg",
          name: "Silviu Popovici",
          pointsGained: 35,
        },
        {
          id: 10,
          img: "https://campmessenger.com/wp-content/uploads/2019/03/user.png",
          name: "David Mansy",
          pointsGained: 35,
        },
        {
          id: 13,
          img: "https://campmessenger.com/wp-content/uploads/2019/03/user.png",
          name: "Dwayne Wright",
          pointsGained: 44,
        },
        {
          id: 14,
          img: "https://campmessenger.com/wp-content/uploads/2019/03/user.png",
          name: "Denim Mazuki",
          pointsGained: 44,
        },
        {
          id: 15,
          img:
            "https://images.pexels.com/photos/1002008/pexels-photo-1002008.jpeg",
          name: "Christian Eriebach",
          pointsGained: 44,
        }
      ],
    };
  },
};
</script>

<style>
.user-card {
  background:  #f3f3f3;
  margin: 2px 0;
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 1rem 1.5rem;
}

.user-card> div:nth-of-type(1) {
    display: flex;
    align-items: center;
    font-weight: 600;
}

.user-card> div:nth-of-type(1)> span:nth-of-type(1) {
    width: 80px;
    color:  #cbcbcc;
}

.user-card> div:nth-of-type(2) {
    font-weight: 600;
}

img {
  width: 30px;
  height: 30px;
  border-radius: 50%;
  border: 2px solid #cbcbcc;
  margin-right: 1rem;
}

.username {
    color: #555555;
}

.lead-footer {
  background: white;
  padding: 2rem 1rem;
  text-align: center;
  font-weight: 600;
  color:  #555555;
}
</style>
