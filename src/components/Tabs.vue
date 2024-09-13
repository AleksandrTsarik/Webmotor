<template>
  <div class="tab">
    <div class="tab-name">
      <div
        v-for="(item, i) in tabNameContent"
        :key="i"
        class="tab-name__item"
        @click="tab = item.tabNumb"
        :class="tab === item.tabNumb ? 'active' : ''"
      >
        <div class="tab-name__title">{{ item.title }}</div>
        <div class="tab-name__content tab-text">{{ item.text }}</div>
      </div>
    </div>
    <div class="tab-content">
      <div class="tab-content__inner">
        <div class="tab-content__item" v-if="tab === 'tab-1' ">
          <div class="tab-content__title">Контент таба 1</div>
          <div class="tab-content__inner">
            <div class="tab-content__text tab-text">Безусловно, начало повседневной работы по формированию позиции способствует подготовке и реализации модели развития. </div>
            <div class="tab-content__list">
              <ul>
                <li>Элемент ненумерованного списка</li>
                <li>Элемент ненумерованного списка</li>
                <li>Элемент ненумерованного списка</li>
              </ul>
            </div>
            <div class="tab-content__text tab-text">Безусловно, начало повседневной работы по формированию позиции способствует подготовке и реализации модели развития. </div>
            <div class="tab-content__list">
              <ol>
                <li>Элемент нумерованного списка</li>
                <li>Элемент нумерованного списка</li>
                <li>Элемент нумерованного списка</li>
              </ol>
            </div>
            <div class="tab-content__text tab-text">Безусловно, начало повседневной работы по формированию позиции способствует подготовке и реализации модели развития. </div>
            <div class="tab-content__text tab-text">Безусловно, начало повседневной работы по формированию позиции способствует подготовке и реализации модели развития. </div>
            <div class="tab-content__list">
              <ul>
                <li>Элемент ненумерованного списка</li>
                <li>Элемент ненумерованного списка</li>
                <li>Элемент ненумерованного списка</li>
              </ul>
            </div>
            <div class="tab-content__text tab-text">Безусловно, начало повседневной работы по формированию позиции способствует подготовке и реализации модели развития. </div>
            <div class="tab-content__list">
              <ol>
                <li>Элемент нумерованного списка</li>
                <li>Элемент нумерованного списка</li>
                <li>Элемент нумерованного списка</li>
              </ol>
            </div>
            <div class="tab-content__text tab-text">Безусловно, начало повседневной работы по формированию позиции способствует подготовке и реализации модели развития. </div>
          </div>
        </div>
        <div class="tab-content__item" v-else-if="tab === 'tab-2' ">
          <div class="tab-content__title">Контент таба 2</div>
          <div class="tab-content__inner">
            <Input :type="'text'" :placeholder="'Имя*'" />
            <Input :type="'tel'" :placeholder="'Телефон*'" />
            <Input :type="'email'" :placeholder="'E-mail*'" required />
          </div>
        </div>
        <div class="tab-content__item" v-else-if="tab === 'tab-3' ">
          <div class="tab-content__title">Контент таба 3</div>
          <div class="tab-content__inner">
            <div class="tab-content__text tab-text">Безусловно, начало повседневной работы по формированию позиции способствует подготовке и реализации модели развития. </div>
            <div class="tab-content__list">
              <ul>
                <li>Элемент ненумерованного списка</li>
                <li>Элемент ненумерованного списка</li>
                <li>Элемент ненумерованного списка</li>
              </ul>
            </div>
            <div class="tab-content__text tab-text">Безусловно, начало повседневной работы по формированию позиции способствует подготовке и реализации модели развития. </div>
            <div class="tab-content__list">
              <ol>
                <li>Элемент нумерованного списка</li>
                <li>Элемент нумерованного списка</li>
                <li>Элемент нумерованного списка</li>
              </ol>
            </div>
            <div class="tab-content__text tab-text">Безусловно, начало повседневной работы по формированию позиции способствует подготовке и реализации модели развития. </div>
            <div class="tab-content__text tab-text">Безусловно, начало повседневной работы по формированию позиции способствует подготовке и реализации модели развития. </div>
            <div class="tab-content__list">
              <ul>
                <li>Элемент ненумерованного списка</li>
                <li>Элемент ненумерованного списка</li>
                <li>Элемент ненумерованного списка</li>
              </ul>
            </div>
            <div class="tab-content__text tab-text">Безусловно, начало повседневной работы по формированию позиции способствует подготовке и реализации модели развития. </div>
            <div class="tab-content__list">
              <ol>
                <li>Элемент нумерованного списка</li>
                <li>Элемент нумерованного списка</li>
                <li>Элемент нумерованного списка</li>
              </ol>
            </div>
            <div class="tab-content__text tab-text">Безусловно, начало повседневной работы по формированию позиции способствует подготовке и реализации модели развития. </div>
          </div>
        </div>
      </div>
      <div class="tab-content__btn">
        <Button class="btn-dark" :label="'Кнопка действия'" :type="'submit'" />
      </div>
     
    </div>
  </div>
</template>

<script>
import Button from '../components/UI/Button.vue'
import Input from '../components/UI/Input.vue'
export default {
  components: {
    Button,
    Input
  },
  data() {
    return {
      tab: 'tab-1',
      tabNameContent: [
        {
          title: 'Заголовок таба 1',
          text: 'Равным образом, высококачественный прототип будущего проекта способствует повышению качества анализа существующих паттернов ',
          tabNumb: 'tab-1'
        },
        {
          title: 'Заголовок таба 2',
          text: 'Равным образом, высококачественный прототип будущего проекта способствует повышению качества анализа существующих паттернов ',
          tabNumb: 'tab-2'
        },
        {
          title: 'Заголовок таба 3',
          text: 'Равным образом, высококачественный прототип будущего проекта способствует повышению качества анализа существующих паттернов ',
          tabNumb: 'tab-3'
        },
      ]
    }
  }
}
</script>

<style lang="scss" scoped>
  .tab {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 45px;
    height: 47vh;
    @media(max-width: 991px) {
      grid-template-columns: 1fr;
      height: 100%;
      gap: 30px;
    }
  }
  .tab-name {
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    &__item {
      background-color: var(--secondary);
      margin-bottom: 20px;
      padding: 25px 20px;
      color: var(--text);
      transition: 0.3s;
      cursor: pointer;
      &:last-child {
        margin-bottom: 0;
      }
      &.active {
        background-color: var(--primary);
        color: var(--bg);
        .tab-text {
          color: var(--bg);
        }
      }
    }
    &__title {
      font-size: 24px;
      font-weight: 500;
      margin-bottom: 25px;
    }
    &__content {}
  }
  .tab-content {
    background-color: var(--secondary);
    padding: 20px;
    position: relative;
    overflow: hidden;
    @media(max-width: 991px) {
      height: 400px;
    }
    &__title {
      font-size: 32px;
      font-weight: 500;
      margin-bottom: 15px;
    }
    &__inner {
      height: 100%;
      overflow-y: auto;
      overflow-x: hidden;
      &::-webkit-scrollbar {
        width: 4px;
      }
      &::-webkit-scrollbar-track {
        background-color: rgba(#ADB6BF66, 0.4);
      }
      &::-webkit-scrollbar-thumb {
        background-color: var(--primary);
        border-radius: 20px;
        border: 1px solid transparent;
        height: 10%;
      }
      > div {
        margin-bottom: 1em;
        &:last-child {
          margin-bottom: 0;
        }
      }
      .block-input {
        max-width: 60%;
        margin-bottom: 25px;
        &:last-child {
          margin-bottom: 0;
        }
      }
    }
    &__item {}
    &__btn {
      position: absolute;
      bottom: 20px;
      left: 20px;
      right: 20px;
      z-index: 10;
      button {
        display: block;
        width: 100%;
      }
    }
    &__list {
      li {
        margin-bottom: 0.2em;
        &:last-child {
          margin-bottom: 0;
        }
      }
      ul {
        list-style-type: disc;
        list-style: inside
      }
      ol {
        list-style-type: none; 
        counter-reset: num;
        li {
          position: relative;
          &:before {
            content: counter(num)'.';
            counter-increment: num;
            margin-right: 0.8em;
          }
        }
      }
    }
  }
  .tab-text {
    font-size: 16px;
    font-weight: 400;
    color: var(--text);
  }
</style>