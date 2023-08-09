<template>
  <div class="sidebar-block">
    <div class="categories">
      <ul class="category-list">
        <li class="category-label">
          <span>Название категории</span>
          <span class="attribute-number">3</span>
        </li>
        <li class="category-name">
          <span>Название категории</span>
          <span class="attribute-number">3</span>
        </li>
        <li class="category-name">
          <span>Название категории</span>
          <span class="attribute-number">3</span>
        </li>
        <li class="category-name">
          <span>Название категории</span> <span>3</span>
        </li>
      </ul>
    </div>
    <div class="cost-filter">
      <span>Цена</span>
      <div class="from-to">
        <input type="text" class="from" placeholder="от 5500 ₽" />
        <div class="divider"></div>
        <input type="text" class="to" placeholder="до 5500 ₽" />
      </div>
    </div>
    <div class="brands-filter">
      <div class="brands-filter-header">
        <span>Бренд</span>
        <button>Очистить</button>
      </div>
      <input type="text" placeholder="Поиск" class="filter-search-bar" />
      <div class="attributes-checkbox">
        <div class="checkbox">
          <div class="checkbox-left">
            <input
              type="checkbox"
              id="input-checkbox-1"
              class="input-checkbox"
            />
            <label for="input-checkbox-1">Атрибут</label>
          </div>
          <span class="attribute-number">3</span>
        </div>
        <div class="checkbox">
          <div class="checkbox-left">
            <input
              type="checkbox"
              id="input-checkbox-2"
              class="input-checkbox"
            />
            <label for="input-checkbox-2">Атрибут</label>
          </div>
          <span class="attribute-number">3</span>
        </div>
        <div class="checkbox">
          <div class="checkbox-left">
            <input
              type="checkbox"
              id="input-checkbox-3"
              class="input-checkbox"
            />
            <label for="input-checkbox-3">Атрибут</label>
          </div>
          <span class="attribute-number">3</span>
        </div>
        <div class="checkbox">
          <div class="checkbox-left">
            <input
              type="checkbox"
              id="input-checkbox-4"
              class="input-checkbox"
            />
            <label for="input-checkbox-4">Атрибут</label>
          </div>
          <span class="attribute-number">3</span>
        </div>
        <div class="checkbox">
          <div class="checkbox-left">
            <input
              type="checkbox"
              id="input-checkbox-5"
              class="input-checkbox"
            />
            <label for="input-checkbox-5">Атрибут</label>
          </div>
          <span class="attribute-number">3</span>
        </div>
        <div class="checkbox">
          <div class="checkbox-left">
            <input
              type="checkbox"
              id="input-checkbox-6"
              class="input-checkbox"
            />
            <label for="input-checkbox-6">Атрибут</label>
          </div>
          <span class="attribute-number">3</span>
        </div>
      </div>
    </div>
    <div class="size-filter">
      <span class="size">Размер</span>
      <div class="attributes-checkbox">
        <div class="checkbox">
          <div class="checkbox-left">
            <input
              type="checkbox"
              id="input-checkbox-7"
              class="input-checkbox"
            />
            <label for="input-checkbox-7">Атрибут</label>
          </div>
          <span class="attribute-number">3</span>
        </div>
        <div class="checkbox">
          <div class="checkbox-left">
            <input
              type="checkbox"
              id="input-checkbox-8"
              class="input-checkbox"
            />
            <label for="input-checkbox-8">Атрибут</label>
          </div>
          <span class="attribute-number">3</span>
        </div>
        <div class="checkbox">
          <div class="checkbox-left">
            <input
              type="checkbox"
              id="input-checkbox-9"
              class="input-checkbox"
            />
            <label for="input-checkbox-9">Атрибут</label>
          </div>
          <span class="attribute-number">3</span>
        </div>
        <div class="checkbox">
          <div class="checkbox-left">
            <input
              type="checkbox"
              id="input-checkbox-10"
              class="input-checkbox"
            />
            <label for="input-checkbox-10">Атрибут</label>
          </div>
          <span class="attribute-number">3</span>
        </div>
        <div class="checkbox">
          <div class="checkbox-left">
            <input
              type="checkbox"
              id="input-checkbox-11"
              class="input-checkbox"
            />
            <label for="input-checkbox-11">Атрибут</label>
          </div>
          <span class="attribute-number">3</span>
        </div>
        <div class="checkbox">
          <div class="checkbox-left">
            <input
              type="checkbox"
              id="input-checkbox-12"
              class="input-checkbox"
            />
            <label for="input-checkbox-12">Атрибут</label>
          </div>
          <span class="attribute-number">3</span>
        </div>
      </div>
    </div>
  </div>
</template>

<script></script>

<style lang="scss" scoped>
@import url("https://fonts.googleapis.com/css2?family=PT+Sans:wght@400;700&display=swap");

@media screen and (max-width: 1920px) {
  .attribute-number {
    color: #aaa;
    padding-right: 16px;
  }
  .sidebar-block {
    font-family: "PT Sans", sans-serif;
    height: auto;
    width: 280px;
    display: flex;
    flex-direction: column;
    gap: 28px;

    .categories {
      display: flex;
      font-family: PT Sans;
      font-size: 14px;
      font-style: normal;
      font-weight: 400;
      line-height: 16px;

      .category-list {
        padding: 0;
        display: flex;
        width: 100%;
        flex-direction: column;

        .category-label {
          display: flex;
          height: 30px;
          padding: 0px 16px 0px 8px;
          justify-content: space-between;
          align-items: center;
          align-self: stretch;
        }

        .category-name {
          display: flex;
          height: 30px;
          padding: 0px 16px 0px 32px;
          justify-content: space-between;
          align-items: center;
          align-self: stretch;

          :first-child:hover {
            color: #7397f5;
          }
        }
        :nth-child(4) {
          border-radius: 5px;
          background-color: #e2efff;
          :nth-child(2) {
            margin-right: 16px;
          }
        }
      }
    }

    .cost-filter {
      display: flex;
      flex-direction: column;
      align-items: center;
      span {
        color: #333;
        font-family: PT Sans;
        font-size: 16px;
        font-style: normal;
        font-weight: 700;
        line-height: 20px;
      }
      .from-to {
        display: flex;
        gap: 16px;
        margin-top: 16px;
        align-items: center;
        .from,
        .to {
          width: 100%;
          display: flex;
          padding: 10px 8px;
          align-items: center;
          gap: 6px;
          flex: 1 0 0;
          border-radius: 4px;
          border: 1px solid #d5d5d5;
          background: #fff;
        }
        .divider {
          width: 10px;
          height: 1px;
          background: #d5d5d5;
        }

        .from::placeholder,
        .to::placeholder {
          color: #333;
          font-family: PT Sans;
          font-size: 14px;
          font-style: normal;
          font-weight: 400;
          line-height: 16px;
        }

        .from:focus,
        .to:focus {
          border-color: #3aafdd;
          outline: 0;
          box-shadow: 0 0 0 0.1rem rgba(94, 146, 224, 0.418);
        }

        :focus::-webkit-input-placeholder {
          color: transparent;
        }
      }
    }
    .brands-filter {
      display: flex;
      flex-direction: column;
      gap: 16px;

      .brands-filter-header {
        display: flex;
        justify-content: space-between;
        span {
          color: #333;
          font-family: PT Sans;
          font-size: 16px;
          font-style: normal;
          font-weight: 700;
          line-height: 20px;
        }
        button {
          color: #aaa;
          background: none;
          border: none;
          text-align: right;
          font-family: PT Sans;
          font-size: 12px;
          font-style: normal;
          font-weight: 400;
          line-height: 12px;
          text-decoration-line: underline;
        }
        button:hover {
          color: #333;
          text-align: right;
          font-family: PT Sans;
          font-size: 12px;
          font-style: normal;
          font-weight: 400;
          line-height: 12px;
          text-decoration-line: underline;
        }
      }
      .filter-search-bar {
        display: flex;
        padding: 10px 12px;
        align-items: flex-start;
        gap: 8px;
        align-self: stretch;
        border-radius: 4px;
        border: 1px solid #d5d5d5;
      }

      .filter-search-bar::placeholder {
        padding-left: 28px;
        background: url("../assets/header-imgs/search-icon-blend.svg") no-repeat;
      }

      .filter-search-bar:focus {
        border-color: #7397f5;
        outline: 0;
        font-family: PT Sans;
        font-size: 14px;
        font-style: normal;
        font-weight: 400;
        line-height: 16px;
      }
      :focus::-webkit-input-placeholder {
        color: transparent;
        background: none;
      }
    }
    .size-filter {
      display: flex;
      flex-direction: column;
      gap: 16px;

      .size {
        display: flex;
        justify-content: center;
        color: #333;
        font-family: PT Sans;
        font-size: 16px;
        font-style: normal;
        font-weight: 700;
        line-height: 20px;
      }
    }
    .attributes-checkbox {
      display: flex;
      flex-direction: column;
      gap: 12px;

      .checkbox {
        display: flex;
        align-items: center;
        justify-content: space-between;
        width: 100%;

        .checkbox-left {
          display: flex;
          align-items: center;

          .input-checkbox {
            display: none;
          }

          label {
            color: #333;
            font-family: PT Sans;
            font-size: 14px;
            font-style: normal;
            font-weight: 400;
            line-height: 16px;
            display: inline-flex;
            gap: 12px;
            align-items: center;
            user-select: none;

            &::before {
              content: "";
              display: inline-block;
              width: 1.3em;
              height: 1.3em;
              flex-shrink: 0;
              flex-grow: 0;
              border: 1px solid #d5d5d5;
              border-radius: 3px;
              background-repeat: no-repeat;
              background-position: center center;
            }
          }

          label:hover::before {
            border-color: #7397f5;
          }

          .input-checkbox[type="checkbox"]:checked + label::before {
            background-image: url("../assets/sidebar-imgs/checked.svg");
          }
        }
      }
    }
  }
}

@media (max-width: 375px) {
  .sidebar-block {
    display: none;
  }
}
</style>
