<template>
  <div class="user-profile q-mb-lg">
    <div class="user-info flex column flex-center">
      <q-avatar class="user-avatar q-mb-sm" size="9.6rem">
        <img :src="profileImage" />
      </q-avatar>
      <div class="text-group flex column flex-center">
        <strong class="user-name text-h4 text-weight-bold q-mb-xs q-mb-md-md">
          Hwang Sang-eun <q-icon name="check_circle" color="blue"></q-icon>
        </strong>
        <div class="lt-md">Developer</div>
        <div class="user-detail gt-sm">
          <button @click="copyEmail" class="user-email" type="button">
            <i class="fa-regular fa-envelope q-mr-xs"></i> sanggusseu@gmail.com
          </button>
          <span class="user-job text-weight-bold text-primary">
            <i class="fa-solid fa-code"></i>
            Developer
          </span>
        </div>
      </div>
    </div>
    <div class="actions flex flex-center q-mt-xs q-mt-md-sm">
      <a href="https://github.com/sanggusseu" target="_blank">
        <i class="fa-brands fa-square-github"></i>
        깃허브
      </a>
      <button @click="copyURL" type="button">
        <i class="fa-solid fa-share-nodes"></i>
        공유하기
      </button>
      <a href="mailto:sanggusseu@gmail.com">
        <i class="fa-solid fa-envelope"></i>
        이메일
      </a>
    </div>
  </div>
</template>

<script setup>
import profileImage from '../assets/images/profile.jpg';
const copyClipboard = (text, message) => {
  navigator.clipboard.writeText(text).then(() => alert(message));
};

const copyEmail = () => {
  copyClipboard('sanggusseu@gmail.com', '이메일 주소가 복사되었습니다.');
};

const copyURL = () => {
  copyClipboard('https://sanggusseu.github.io/', 'URL이 복사되었습니다.');
};
</script>

<style lang="scss" scoped>
.user-avatar img {
  object-fit: cover;
}

.user-email {
  height: 3.6rem;
  padding: 0 1.2rem;
  font-size: 1.4rem;
  color: #565e6c;
  background-color: #f3f4f6;
  border-radius: 1.8rem;
}

.actions a:hover,
.actions button:hover {
  background-color: $secondary;
  border-radius: 0.4rem;
}

@media (min-width: $breakpoint-sm) {
  .user-profile {
    display: flex;
    align-items: center;
    justify-content: space-between;
  }

  .user-info {
    flex-direction: row;
    gap: 3.2rem;
  }

  .user-avatar {
    width: 14.5rem;
    height: 14.5rem;
  }

  .text-group {
    align-items: start;
  }

  .user-name {
    font-size: 3.2rem;
  }

  .user-detail {
    display: flex;
    align-items: center;
    gap: 1.6rem;
  }

  .actions {
    margin-top: 0;
    gap: 1.6rem;
  }
}
</style>
