### 在ivew中 使用Modal弹窗时，如果没有用v-if 结束弹窗的生命周期时，iview css 会无限增加z-index的弹窗值



### 对于在iframe嵌套Vue应用时，在Vue的生命周期mounted 获取URL参数，使用$route.query获取不到链接中的值
  #### 通过想显示iframe src的值
  
  #### // 使用location 获取到hash
  let hash = location.hash;
  #### // 将hash 解码，然后分割出URL中的SearchParams
  let allUrlParams = hash ? decodeURIComponent(hash).split('?')[1]:'';
  #### // 将URL参数放到对应的构造函数中
  let params = new URLSearchParams(allUrlParams);
  #### // 选择性获取对应的参数值
    let token=params.get('token'),rt=params.get('rt');

### 遇到微应用，涉及内网和外网访问，当用内网IP访问时，将所有对应有需要的应用注册微应用时转为对应的IP，外网保持返回结果不变接入微应用


### iview中 使用ToolTip 如果需要换行需要将max-width设置值

### computed的时候假入有计算值报错问题会影响页面后续代码逻辑处理

### iview中 使用Modal z-index的值会持续增长，可以通过this.$refs.modal.wrapStyles.zIndex = Number 赋值会固定
