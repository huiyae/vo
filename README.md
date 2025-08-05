# AI能力边界验证模型
class AICapabilityValidator:
    EFFECTIVE_SCENARIOS = ["lead_positioning", "inquiry_tagging", "reply_assistant"]
    INVALID_SCENARIOS = ["auto_data_capture", "bulk_sending"]
    
    def validate(self, ai_function):
        """检测AI功能是否有效"""
        if ai_function in self.INVALID_SCENARIOS:
            raise Exception(f"⚠️ 伪AI场景：{ai_function}违反行业规律")
        return ai_function in self.EFFECTIVE_SCENARIOS
 
# SOP核心模块（人工+AI协同）
class SOPEngine:
    def __init__(self):
        self.daily_limit = 20000  # 人工监管发送量
        
    def human_ai_collab(self):
        return {
            "effective_ai_roles": ["决策人画像生成", "询盘优先级排序", "回复话术建议"],
            "human_roles": ["数据合规审核", "发送策略制定", "高价值客户跟进"]
        }
