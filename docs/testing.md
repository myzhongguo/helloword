# 测试文档

## 测试策略
- 单元测试：使用 Jest + React Testing Library
- 集成测试：使用 Cypress
- E2E 测试：使用 Playwright
- 性能测试：使用 Lighthouse

## 测试覆盖率要求
- 组件测试覆盖率：≥ 80%
- 工具函数测试覆盖率：≥ 90%
- API 测试覆盖率：≥ 95%

## 测试用例示例

### 组件测试
```javascript
import { render, screen } from '@testing-library/react';
import Button from './Button';

test('renders button with correct text', () => {
  render(<Button>Click me</Button>);
  const buttonElement = screen.getByText(/Click me/i);
  expect(buttonElement).toBeInTheDocument();
});
```

### API 测试
```javascript
describe('GET /api/user', () => {
  it('should return user info', async () => {
    const res = await request(app)
      .get('/api/user')
      .set('Authorization', 'Bearer valid_token');
    
    expect(res.statusCode).toEqual(200);
    expect(res.body).toHaveProperty('username');
  });
});
```

## 测试流程
1. 本地开发时运行单元测试
2. 提交代码前运行所有测试
3. CI/CD 流水线中运行完整测试套件
4. 生成测试覆盖率报告
5. 修复所有失败的测试用例
