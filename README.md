name: Claude Code


      - name: Run Claude Code
        id: claude
        uses: anthropics/claude-code-action@v1
        env:
          # 设置国产模型兼容 Anthropic 格式的 API 地址
          # 示例使用 DeepSeek 的兼容地址，请根据实际模型文档修改
          ANTHROPIC_BASE_URL: "https://open.bigmodel.cn/api/anthropic"
        with:
          #claude_code_oauth_token: ${{ secrets.ANTHROPIC_API_KEY }} #官方模型
          claude_code_oauth_token: ${{ secrets.ZHIPU_API_KEY }}
          #ANTHROPIC_BASE_URL
          #anthropic_base_url: https://open.bigmodel.cn/api/anthropic
          # Optional: Customize the trigger phrase (default: @claude)
          # trigger_phrase: "/claude"

          # Optional: Trigger when specific user is assigned to an issue
          # assignee_trigger: "claude-bot"

          # Optional: Configure Claude's behavior with CLI arguments
          # claude_args: |
          #   --model claude-opus-4-1-20250805
          #   --max-turns 10
          #   --allowedTools "Bash(npm install),Bash(npm run build),Bash(npm run test:*),Bash(npm run lint:*)"
          #   --system-prompt "Follow our coding standards. Ensure all new code has tests. Use TypeScript for new files."

          # Optional: Advanced settings configuration
          # settings: |
          #   {
          #     "env": {
          #       "NODE_ENV": "test"
          #     }
          #   }
