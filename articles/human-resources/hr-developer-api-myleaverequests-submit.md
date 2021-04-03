---
title: إرسال طلب إجازة إلى سير العمل
description: في Microsoft Dynamics 365 Human Resources، يمكنك استخدام واجهة برمجه التطبيقات MyLeaveRequests submit() لإرسال طلب الإجازة إلى سير العمل.
author: andreabichsel
manager: tfehr
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: aeb3d66ad24f96efea1b0ea9828a537f8853c94b
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/17/2021
ms.locfileid: "5465476"
---
# <a name="submit-a-leave-request-to-workflow"></a>إرسال طلب إجازة إلى سير العمل

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

في Microsoft Dynamics 365 Human Resources، يمكنك استخدام واجهة برمجه التطبيقات MyLeaveRequests submit() لإرسال طلب الإجازة إلى سير العمل. يتم كشف واجة API هذه كإجراء على كيان MyLeaveRequests OData.

## <a name="prerequisites"></a>المتطلبات الأساسية

يجب حفظ طلب الإجازة في قاعده البيانات ويجب أن تكون قابلا للاسترداد من خلال كيان MyLeaveRequests.

## <a name="permissions"></a>أذونات

أحد الأذونات التالية مطلوب لاستدعاء واجهة API هذه. لمزيد من المعلومات حول الأذونات وكيفية إعدادها، راجع [التخويل](hr-developer-api-authentication.md).

| نوع الإذن                    | الأذونات (من الأقل امتيازًا إلى الأكثر امتيازًا) |
|------------------------------------|--------------------------------------------------------|
| مفوض (حساب عمل أو مدرسة) | user\_impersonation                                    |

## <a name="https-request"></a>طلب HTTPS

<!-- { "blockType": "ignored" } -->
```HTTP
POST https://{cluster}.hr.talent.dynamics.com/namespaces/{namespace_guid}/data/MyLeaveRequests(RequestId='{requestId}', LeaveType='{leaveType}', LeaveDate={leaveDate}, dataAreaId={dataArea})/Microsoft.Dynamics.DataEntities.submit?cross-company=true
```

يتوافق الطلب مع مقاييس OData. تشير المعلمات {requestId} و {leaveType} و {leaveDate}و {dataArea} إلى الحقول التي تشكل المفتاح الطبيعي المركب لكيان MyLeaveRequests.

> [!NOTE]
> بينما تشير حقول الكيان MyLeaveRequests إلى بند فردي في طلب الإجازه، فان استدعاء واجهة API الخاصة بالإرسال سيرسل طلب الإجازة كاملاً (كافة البنود) إلى سير العمل.

### <a name="request-headers"></a>رؤوس الطلبات

| رأس         | قيمة                     |
|----------------|---------------------------|
| التخويل  | الحامل {token} (مطلوب) |
| نوع المحتوى   | application/json          |

### <a name="request-body"></a>نص الطلب

لا تقم بتقديم نص طلب لهذا الأسلوب.

### <a name="response"></a>استجابة

الاستجابة الناجحة دائمًا هي استجابة **لا يوجود محتوى 204**.

سيتلقى المتصلون غير المصرح لهم الرد **غير مصرح 401** أو **ممنوع 403**.

إذا لم تنجح عملية التسليم (بسبب التحقق من الصحة، على سبيل المثال) ، فان الاستجابة ستكون **خطأ في الخادم 500**، وسيتضمن نص الاستجابة كائن JSON مع مزيد من التفاصيل.

## <a name="example"></a>مثال

```http
POST https://aos-rts-sf-550e5c091f6-prod-westus2.hr.talent.dynamics.com/namespaces/b2eb8003-334f-4a84-ab63-edbe23569090/data/MyLeaveRequests(RequestId='USMF-000065', LeaveType='Vacation', LeaveDate=2019-10-04T12:00:00Z, dataAreaId='USMF')/Microsoft.Dynamics.DataEntities.submit
```

```json
{
  "error": {
    "code": "",
    "message": "An error has occurred.",
    "innererror": {
      "message": "Exception occurred while executing action submit on Entity MyLeaveRequest: The request would put the 'Vacation' balance below the allowed minimum balance on 9/10/2019.",
      "type": "System.InvalidOperationException",
      "stacktrace": "   at Microsoft.Dynamics.Platform.Integration.Services.OData.Action.ActionInvokable.Invoke()   at Microsoft.Dynamics.Platform.Integration.Services.OData.Update.UpdateProcessor.ActionInvocation(ChangeOperationContext context, ActionInvokable action)   at Microsoft.Dynamics.Platform.Integration.Services.OData.Update.UpdateManager.<>c__DisplayClass13_0.<ScheduleInvokable>b__0(ChangeOperationContext context)   at Microsoft.Dynamics.Platform.Integration.Services.OData.Update.ChangeInfo.ExecuteActionsInCompanyContext(IEnumerable`1 actionList, ChangeOperationContext operationContext)\r\n   at Microsoft.Dynamics.Platform.Integration.Services.OData.Update.ChangeInfo.ExecuteActions(ChangeOperationContext context)   at Microsoft.Dynamics.Platform.Integration.Services.OData.Update.UpdateManager.SaveChanges()   at Microsoft.Dynamics.Platform.Integration.Services.OData.AxODataDelegatingHandler.<SaveChangesAsync>d__3.MoveNext()"
    }
  }
}
```

## <a name="validation-and-error-messages"></a>رسائل التحقق من الصحة ورسائل الخطأ

كجزء من استدعاء API الخاص بالإرسال، تتحقق الموارد البشرية من صحة منطق العمل قبل الإرسال، مما يضمن وجود طلب الإجازة في حالة صالحة للإرسال. رسائل الخطأ المحتملة التي قد تتلقاها في الاستجابة إذا فشلت عملية التحقق من الصحة:

 - قد يضع الطلب الرصيد '{LeaveTypeId}' تحت الحد الأدنى للرصيد المسوح به في {date}.
 - لا يمكن إرسال طلب زمن التوقف في حالة مكتملة.
 - لا يمكن إرسال طلب أو حفظه لأنه لم يتم إجراء أية تغييرات. قم بإضافة أو تحديث المبلغ أو نوع الإجازة ثم حاول مرة أخرى.
 - طلب زمن التوقف الذي أدخلته يحتوي على يوم واحد أو أكثر بنفس التاريخ ونوع الإجازة كطلب معلق موجود. الرجاء استدعاء الطلب الموجود لإجراء التغييرات.
 - لا ينطبق رمز السبب '{ReasonCodeId}' على أي من أنواع الإجازات في الطلب.
 - يتطلب نوع الإجازة '{LeaveTypeId}' رمز سبب. حدد النوع المناسب ورمز السبب.
 - لم يتم إرسال زمن التوقف بنجاح. تم حفظ زمن التوقف كطلب مسودة.

## <a name="see-also"></a>راجع أيضًا

- [نظره عامة على MyLeaveRequests](hr-developer-api-myleaverequests-overview.md)
- [المصادقة](hr-developer-api-authentication.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]