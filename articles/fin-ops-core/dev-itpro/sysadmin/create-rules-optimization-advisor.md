---
title: إنشاء قواعد مرشد التحسين
description: تناقش هذه المقالة كيفية إضافة القواعد الجديدة إلى مرشد التحسين.
author: roxanadiaconu
ms.date: 02/04/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SelfHealingWorkspace
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: sericks
ms.search.validFrom: 2017-12-01
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: 1b1d9b14cb67b1dd0a961f6f8618de37147a2c52
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/03/2022
ms.locfileid: "8850894"
---
# <a name="create-rules-for-optimization-advisor"></a>إنشاء قواعد مرشد التحسين

[!include [banner](../includes/banner.md)]

توضح هذه المقالة كيفية إنشاء القواعد الجديدة **لمرشد التحسين**. على سبيل المثال، يمكنك إنشاء قاعدة جديدة لتحديد حالات طلبات عروض الأسعار‬ (RFQ) التي تشتمل على عنوان فارغ. استخدام العناوين في الحالات يجعل من السهل تحديدها والبحث عنها. بينما هذا المثال بسيط جدًا، يوضح ما يمكن تحقيقه باستخدام قواعد تحسين الأداء. 

*القاعدة* هي علامة اختيار في بيانات التطبيق. إذا تم الوفاء بالشرط الذي تقيمه القاعدة، يتم إنشاء فرص لتحسين العمليات أو البيانات. يمكن تنفيذ الفرص ويمكن قياس تأثير الإجراءات بشكل اختياري. 

لإنشاء قاعدة جديدة لـ **مرشد التحسين**، أضف فئة جديدة توسع الفئة المجردة **SelfHealingRule** وتنفذ واجهة **IDiagnosticsRule** ويتم تزيينها بالسمة **DiagnosticRule**. كما يجب أن تشتمل الفئة على أسلوب مزين بالسمة **DiagnosticsRuleSubscription**. بشكل تقليدي، يتم إجراء هذا في أسلوب **opportunityTitle** الذي ستتم مناقشته لاحقًا. يمكن إضافة هذه الفئة الجديدة إلى نموذج مخصص باستخدام تبعية في نموذج **SelfHealingRules**. في المثال التالي، تُسمى القاعدة الجاري تنفيذها **RFQTitleSelfHealingRule**.

```xpp
[DiagnosticsRule] 
public final class RFQTitleSelfHealingRule extends SelfHealingRule implements IDiagnosticsRule 
{ 
… 
} 
```

تشتمل الفئة المجردة **SelfHealingRule** على أساليب مجردة يجب تنفيذها في الفئات القديمة. الذاكرة الأساسية هي أسلوب **التقييم** الأسلوب الذي يقوم بإرجاع قائمة بالفرص المحددة بواسطة القاعدة. يمكن أن تكون الفرص حسب الكيان القانوني أو يمكن تطبيقها على النظام بالكامل.

```xpp
protected List evaluate() 
{ 
    List results = new List(Types::Record); 
    
    DataArea dataArea; 

    while select id from dataArea 
        where !dataArea.isVirtual 
    { 
        changecompany(dataArea.id) 
        { 
            container result = this.findRFQCasesWithEmptyTitle(); 

            if (conLen(result) > 0) 
            { 
                SelfHealingOpportunity opportunity = this.getOpportunityForCompany(dataArea.Id); 
                opportunity.EvaluationState = SelfHealingEvaluationState::Evaluated; 
                opportunity.Data = result; 
                opportunity.OpportunityDate = DateTimeUtil::utcNow(); 
                
                results.addEnd(opportunity); 
            } 
        } 
    } 
    
    return results; 
} 
```

يدور الأسلوب الموضح أعلاه عبر الشركات ويحدد حالات RFQ بالعناوين الفارغة في أسلوب **findRFQCasesWithEmptyTitle**. إذا تم العثور على حالة واحدة على الأقل، فإنه يتم إنشاء فرصة خاصة بالشركة باستخدام أسلوب **getOpportunityForCompany**. لاحظ أن الحقل **بيانات** في جدول **SelfHealingOpportunity** من نوع **الحاوية**، ولذلك يمكنه أن يحتوي على أي بيانات تتعلق بالمنطق الخاص بهذه القاعدة. يسجل الإعداد **OpportunityDate** مع الطابع الزمني الحالي وقت آخر تقييم للفرصة.  

يمكن أن تكون الفرص عبر الشركة. في هذه الحالة، تكون شركات الدوران غير ضرورية ويجب إنشاء الفرصة باستخدام أسلوب **getOpportunityAcrossCompanies**. 

يعرض الرمز التالي أسلوب **findRFQCasesWithEmptyTitle**، الذي يعرض معرفات حالات طلب عروض الأسعار التي تشتمل على عناوين فارغة.

```xpp
private container findRFQCasesWithEmptyTitle() 
{ 
    container result; 

    PurchRFQCaseTable rfqCase; 
    while select RFQCaseId from rfqCase 
        where rfqCase.Name == '' 
    { 
        result += rfqCase.RFQCaseId; 
    } 
    
    return result; 
} 
```

كما أن هناك أسلوبان يجب استخدامهما هما **opportunityTitle** و **opportunityDetails**. الأول يعرض عنوانًا قصيرًا للفرصة، بينما الأخر يعرض وصفًا تفصيليًا للفرصة، التي قد تشتمل على بيانات.

يظهر العنوان المعروض بواسطة **opportunityTitle** تحت عمود **فرصة التحسين** في مساحة عمل **مرشد التحسين**. كما يظهر كعنوان للجزء الجانبي ويعرض مزيدًا من المعلومات حول الفرصة. بشكل تقليدي، يتم تزيين هذا الأسلوب باستخدام السمة **DiagnosticRuleSubscription** التي تأخذ الوسائط التالية: 

* **منطقة التشخيص** – تعداد من النوع **DiagnosticArea** يصف مساحة التطبيق التي تنتمي إليها القاعدة، مثل **DiagnosticArea::SCM**. 

* **اسم القاعدة** -سلسلة تحتوي على اسم القاعدة. سيظهر هذا الاسم ضمن عمود **اسم القاعدة** في نموذج **قاعدة التحقق من صحة التشخيصات** (**DiagnosticsValidationRuleMaintain**). 

* **معدل تكرار التشغيل‬** – تعداد من النوع **DiagnosticRunFrequency** يصف عدد مرات تشغيل القاعدة المطلوب، مثل **DiagnosticRunFrequency::Daily**. 

* **وصف القاعدة** - سلسلة تحتوي على وصف أكثر تفصيلاً للقاعدة. سيظهر هذا ضمن عمود **وصف القاعدة** في نموذج **قاعدة التحقق من صحة التشخيصات** (**DiagnosticsValidationRuleMaintain**). 

> [!NOTE]
> السمة **DiagnosticRuleSubscription** مطلوبة لكي تعمل القاعدة. وعادةً ما يتم استخدامها في **opportunityTitle**، ولكن يمكنها تزيين أي أسلوب للفئة.

التالي هو مثال للتنفيذ. يتم استخدام السلاسل الأولية لتحقيق البساطة، ولكن يتطلب التنفيذ الصحيح وجود ملصقات. 

```xpp
[DiagnosticsRuleSubscription(DiagnosticsArea::SCM, 
                             'Assign titles to Request for Quotation cases', 
                             DiagnosticsRunFrequency::Daily,  
                             'This rule detects Requests for Quotation with empty titles.')] 
public str opportunityTitle() 
{ 
    return 'Assign titles to Request for Quotation cases'; 
} 
```

يظهر الوصف المعروض بواسطة **opportunityDetails** على الجزء الجانبي ويعرض مزيدًا من المعلومات حول الفرصة. يأخذ هذا الوسيطة **SelfHealingOpportunity** التي هي عبارة عن حقل **بيانات** يمكن استخدامه لتوفير المزيد من التفاصيل حول الفرصة. في المثال، يعرض الأسلوب معرفات حالات RFQ المشتملة على عنوان فارغ. 

```xpp
public str opportunityDetails(SelfHealingOpportunity _opportunity) 
{ 
    str details = ''; 
    container opportunityData = _opportunity.Data; 
    int affectedRFQCasesCount = conLen(opportunityData); 

    if (affectedRFQCasesCount != 0) 
    { 
        details = 'The following Request for Quotation cases have an empty title:\n'; 
        for (int i = 1; i <= affectedRFQCasesCount ; i++) 
        { 
            PurchRFQCaseId rfqCaseId = conPeek(opportunityData, i); 
            details += rfqCaseId + '\n'; 
        } 
    } 

    return details; 
}
```

الأسلوبان المجردان المتبقيان للتنفيد هما **provideHealingAction** و **securityMenuItem**. 

يعرض **provideHealingAction** "حقيق" إذا تم توفير إجراء علاج، وإلا، فإنه يعرض "زائف". في حالة عرض "حقيقي"، يجب تنفيذ الأسلوب **performAction** وإلا سيظهر خطأ. أسلوب **performAction** يأخذ وسيطة **SelfHealingOpportunity**، التي يمكن فيها استخدام البيانات للإجراء. في المثال، يفتح الإجراء **PurchRFQCaseTableListPage** للتصحيح اليدوي. 

```xpp
public boolean providesHealingAction() 
{ 
    return true; 
} 

protected void performAction(SelfHealingOpportunity _opportunity) 
{ 
    new MenuFunction(menuItemDisplayStr(PurchRFQCaseTableListPage), MenuItemType::Display).run(); 
} 
```

استنادًا إلى مواصفات القاعدة، قد يكون من الممكن اتخاذ إجراء تلقائي باستخدام بيانات الفرصة. في هذا المثال، قد يستطيع النظام إنشاء عناوين لحالات RFQ تلقائيًا. 

يعرض **securityMenuItem** اسم عنصر قائمة إجراءات لأن القاعدة تكون مرئية فقط للمستخدمين الذين يمكنهم الوصول إلى عنصر قائمة الإجراءات. قد يتطلب الأمان إمكانية وصول المستخدمين المصرح لهم فقط إلى الفرص والقواعد الخاصة. في المثال، يستطيع فقط المستخدمون الذين لديهم وصول إلى **PurchRFQCaseTitleAction** عرض الفرصة. لاحظ أن عنصر قائمة الإجراءات هذا تم إنشاؤه لهذا المثال، وتمت إضافته كنقطة إدخال لامتياز أمان **PurchRFQCaseTableMaintain**. 

> [!NOTE]
> يجب أن يكون عنصر القائمة عبارة عن عنصر قائمة إجراءات لكي يعمل الأمان بشكل صحيح. لن تعمل أنواع عناصر القائمة الأخرى، مثل **عرض عناصر القائمة** بشكل صحيح.

```xpp
public MenuName securityMenuItem() 
{ 
    return menuItemActionStr(PurchRFQCaseTitleAction); 
}
```

بعد تأليف القاعدة، قم بتنفيذ الوظيفة التالية لعرضها في واجهة المستخدم (UI).

```xpp
class ScanNewRulesJob 
{         
    public static void main(Args _args) 
    {         
        SysExtensionCache::clearAllScopes(); 
        var controller = new DiagnosticsRuleController(); 
        controller.runOperation(); 
    } 
} 
```

ستظهر القاعدة في نموذج **قاعدة التحقق من صحة التشخيصات**، وهي متوفرة من **إدارة النظام** > **المهام الدورية** > **صيانة قاعدة التحقق من صحة التشخيصات**. ولتقييمها، انتقل إلى **إدارة النظام** > **المهام الدورية** > **قاعدة التحقق من صحة تشخيصات الجدول‬**، وحدد عدد مرات تكرار القاعدة، مثل **يوميًا**. وانقر فوق **موافق**. انتقل إلى **إدارة النظام** > **مرشد التحسين** لعرض الفرصة الجديدة. 

المثال التالي عبارة عن أجزاء من تعليمات برمجية مع إطار عمل قاعدة تتضمن كافة الأساليب والسمات المطلوبة. من شأنه أن يساعدك في بدء كتابة قواعد جديدة. التسميات وعناصر قائمة الإجراءات المستخدمة في المثال هي مستخدمة فقط لأغراض العرض التوضيحي.

```xpp
[DiagnosticsRuleAttribute]
public final class SkeletonSelfHealingRule extends SelfHealingRule implements IDiagnosticsRule
{
    [DiagnosticsRuleSubscription(DiagnosticsArea::SCM,
                                 "@SkeletonRuleLabels:SkeletonRuleTitle", // Label with the title of the rule
                                 DiagnosticsRunFrequency::Monthly,
                                 "@SkeletonRuleLabels:SkeletonRuleDescription")] // Label with a description of the rule
    public str opportunityTitle()
    {
        // Return a label with the title of the opportunity
        return "@SkeletonRuleLabels:SkeletonOpportunityTitle";
    }

    public str opportunityDetails(SelfHealingOpportunity _opportunity)
    {
        str details = "";

        // Use _opportunity.data to provide details on the opportunity

        return details;
    }

    protected List evaluate()
    {
        List results = new List(Types::Record);

        // Write here the core logic of the rule

        // When creating an opportunity, use:
        //     * this.getOpportunityForCompany() for company specific opportunities
        //     * this.getOpportunityAcrossCompanies() for cross-company opportunities

        return results;
    }

    public boolean providesHealingAction()
    {
        return true;
    }

    protected void performAction(SelfHealingOpportunity _opportunity)
    {
        // Place here the code that performs the healing action

        // To open a form, use the following:
        // new MenuFunction(menuItemDisplayStr(SkeletonRuleDisplayMenuItem), MenuItemType::Display).run();
    }

    public MenuName securityMenuItem()
    {
        return menuItemActionStr(SkeletonRuleActionMenuItem);
    }

}
```

لمزيد من المعلومات، شاهد مقطع الفيديو القصير على YouTube: [مرشد التحسين في Dynamics 365 for Finance and Operations](https://www.youtube.com/watch?v=MRsAzgFCUSQ)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]