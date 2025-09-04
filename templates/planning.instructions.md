---
---
applyTo: "[Target Directory or File Glob]"
---

# [Project Name]: [Module/Feature] - Planning Strategy Template

## 🎯 Strategic Overview

This document outlines the comprehensive strategy for splitting a large refactor or implementation into manageable, focused increments. The goal is to transform an overwhelming change into a series of reviewable, testable, and risk-mitigated steps.

## 📊 Current State Analysis

### **Problem Context**
- **Original Implementation**: [Description of original state]
- **Current Scope**: [Description of current scope]
- **Challenge**: [Key challenges]
- **Solution**: [High-level solution/strategy]

### **Architecture Transition**
```
FROM: [Original architecture description]
TO: [Target architecture description]
├── [Module/Component 1]
│   ├── [File 1]
│   ├── [File 2]
│   └── ...
├── [Module/Component 2]
│   ├── [File 1]
│   └── ...
└── ...
```

## 🚀 Implementation Strategy

### **Phase 1: [Phase Name]**

#### **Objective**: [Phase objective]
#### **Approach**: [Phase approach]
#### **Risk Level**: [Risk level] - [Risk description]

### **Phase 2: [Phase Name]**

#### **Objective**: [Phase objective]
#### **Approach**: [Phase approach]
#### **Risk Level**: [Risk level] - [Risk description]

### **Phase N: [Phase Name]**

#### **Objective**: [Phase objective]
#### **Approach**: [Phase approach]
#### **Risk Level**: [Risk level] - [Risk description]

## 📋 Detailed Implementation Plan

### **[Increment/PR #1]: [Increment Name/Description]**
*Branch: `[branch-name]`*

**Purpose**: [Purpose of increment]
**Scope**: [Scope of increment]
**Duration**: `[duration estimate]`
**Complexity**: `[complexity level]`

**Files to Create**:
```
[Directory/Module]/
├── [File 1]
├── [File 2]
└── ...
```

**Key Tasks**:
- [ ] [Task 1]
- [ ] [Task 2]
- [ ] ...

**Critical Preservation Points**:
- [ ] [Preservation point 1]
- [ ] [Preservation point 2]

**Success Criteria**:
- ✅ [Success criteria 1]
- ✅ [Success criteria 2]

---

### **[Increment/PR #N]: [Increment Name/Description]**
*Branch: `[branch-name]`*

**Purpose**: [Purpose of increment]
**Scope**: [Scope of increment]
**Duration**: `[duration estimate]`
**Complexity**: `[complexity level]`

**Files to Create**:
```
[Directory/Module]/
├── [File 1]
└── ...
```

**Key Tasks**:
- [ ] [Task 1]
- [ ] ...

**Success Criteria**:
- ✅ [Success criteria 1]

---

## 🧪 Testing Strategy

### **Per-Increment/PR Testing Requirements**

#### **Unit Testing**
- [ ] All extracted functions have corresponding unit tests
- [ ] Mock dependencies appropriately for isolation
- [ ] Test edge cases and error conditions
- [ ] Verify input/output contracts match original

#### **Integration Testing**
- [ ] Module-specific operations work end-to-end
- [ ] Cross-module relationships maintained
- [ ] API endpoints return identical responses
- [ ] Database operations perform correctly

#### **Regression Testing**
- [ ] [Key regression criteria]
- [ ] Performance characteristics maintained
- [ ] Error handling patterns preserved

#### **Full System Testing**
- [ ] All existing tests continue to pass
- [ ] End-to-end workflows unchanged
- [ ] Data consistency across all modules

### **Automated Testing Pipeline**

```yaml
Per-Increment/PR Tests:
  - Unit Tests: [Description]
  - Integration Tests: [Description]
  - Regression Tests: [Description]
  - Performance Tests: [Description]
  - Security Tests: [Description]

Final Integration Tests:
  - Full test suite
  - End-to-end workflows
  - Load testing
  - Memory usage analysis
  - Database performance profiling
```

## 🔍 Quality Assurance

### **Code Review Requirements**

#### **Per-Increment/PR Review Checklist**
- [ ] **Functionality**: Extracted code preserves original behavior
- [ ] **Architecture**: Module follows established patterns
- [ ] **Testing**: Comprehensive test coverage
- [ ] **Documentation**: Clear interfaces and usage examples
- [ ] **Performance**: No degradation in response times or memory usage
- [ ] **Security**: Input validation and error handling maintained

#### **Critical Review Points**
- [ ] [Critical review point 1]
- [ ] [Critical review point 2]

### **Merge Requirements**

#### **Per-Increment/PR Merge Criteria**
- ✅ All automated tests pass
- ✅ Code review approved
- ✅ No regression in key behaviors
- ✅ Performance benchmarks met
- ✅ Integration tests pass

#### **Final Integration Merge Criteria**
- ✅ All original tests pass
- ✅ End-to-end workflows unchanged
- ✅ Memory usage within target
- ✅ Database query performance maintained
- ✅ No new security vulnerabilities

## 📈 Risk Management

### **Risk Assessment Matrix**

| Increment/PR | Risk Level | Primary Risks | Mitigation Strategies |
|--------------|-----------|---------------|----------------------|
| [Name/Number] | [Level] | [Risks] | [Mitigation] |
| ...          | ...       | ...           | ...                  |

### **Rollback Strategy**

#### **Per-Increment/PR Rollback**
- **Trigger**: [Trigger condition]
- **Action**: [Rollback action]
- **Timeline**: [Timeline]
- **Recovery**: [Recovery steps]

#### **Emergency Rollback**
- **Trigger**: [Trigger condition]
- **Action**: [Rollback action]
- **Timeline**: [Timeline]
- **Recovery**: [Recovery steps]

## 🎯 Success Metrics

### **Technical Metrics**
- ✅ [Technical metric 1]
- ✅ [Technical metric 2]

### **Quality Metrics**
- ✅ [Quality metric 1]
- ✅ [Quality metric 2]

### **Process Metrics**
- ✅ [Process metric 1]
- ✅ [Process metric 2]

## 📅 Timeline & Milestones

### **Phase 1: [Phase Name] ([Week/Days])**
- [Timeline details]
- **Milestone**: [Milestone description]

### **Phase 2: [Phase Name] ([Week/Days])**
- [Timeline details]
- **Milestone**: [Milestone description]

### **Phase N: [Phase Name] ([Week/Days])**
- [Timeline details]
- **Milestone**: [Milestone description]

## 🎉 Expected Outcomes

### **Immediate Benefits**
- ✅ [Immediate benefit 1]
- ✅ [Immediate benefit 2]

### **Long-term Benefits**
- ✅ [Long-term benefit 1]
- ✅ [Long-term benefit 2]

### **Success Criteria Achievement**
- ✅ [Success criteria 1]
- ✅ [Success criteria 2]

---

This template provides a detailed, generic structure for planning strategies. Replace bracketed placeholders with project-specific details as needed.