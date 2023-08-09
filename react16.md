## jsapi式的 render的时候
  节点方法中 onClick={fun} 这样页面会一直循环事件页面卡死
  正确方式 onClick={()=> fun()} 这样才能解决问题
