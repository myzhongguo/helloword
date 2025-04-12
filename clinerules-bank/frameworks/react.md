# React 开发规范

## 组件开发
- 使用函数组件和 Hooks
- 组件命名采用 PascalCase
- 每个组件单独文件
- 使用 PropTypes 或 TypeScript 进行类型检查
- 保持组件单一职责

## 状态管理
- 优先使用组件内部状态
- 复杂状态使用 Redux Toolkit
- 使用 createSlice 创建 reducer
- 使用 useSelector 和 useDispatch
- 避免直接修改 state

## 性能优化
- 使用 React.memo 优化组件
- 使用 useCallback 缓存回调函数
- 使用 useMemo 缓存计算结果
- 避免不必要的重新渲染
- 使用 React.lazy 实现代码分割

## 代码风格
- 使用 Prettier 统一代码格式
- 使用 ESLint 进行代码检查
- 遵循 Airbnb React 规范
- 使用 JSX 语法糖
- 保持一致的缩进和格式

## 测试规范
- 使用 Jest 进行单元测试
- 使用 React Testing Library 测试组件
- 测试覆盖率 ≥ 80%
- 编写有意义的测试用例
- 测试组件交互和状态变化
