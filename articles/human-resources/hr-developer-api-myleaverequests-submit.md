---
title: إرسال طلب إجازة إلى سير العمل
description: ''
author: andreabichsel
manager: AnnBe
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
ms.openlocfilehash: 008ee231ca9f0459e332b17cea9f2a3f3e3cc2a5
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008006"
---
# <a name="submit-a-leave-request-to-workflow"></a><span data-ttu-id="88607-102">إرسال طلب إجازة إلى سير العمل</span><span class="sxs-lookup"><span data-stu-id="88607-102">Submit a leave request to workflow</span></span>

<span data-ttu-id="88607-103">في Microsoft Dynamics 365 Human Resources، يمكنك استخدام واجهة برمجه التطبيقات MyLeaveRequests submit() لإرسال طلب الإجازة إلى سير العمل.</span><span class="sxs-lookup"><span data-stu-id="88607-103">In Microsoft Dynamics 365 Human Resources, you can use the MyLeaveRequests submit() application programming interface (API) to submit a leave request to workflow.</span></span> <span data-ttu-id="88607-104">يتم كشف واجة API هذه كإجراء على كيان MyLeaveRequests OData.</span><span class="sxs-lookup"><span data-stu-id="88607-104">This API is exposed as an action on the MyLeaveRequests OData entity.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="88607-105">المتطلبات الأساسية</span><span class="sxs-lookup"><span data-stu-id="88607-105">Prerequisites</span></span>

<span data-ttu-id="88607-106">يجب حفظ طلب الإجازة في قاعده البيانات ويجب أن تكون قابلا للاسترداد من خلال كيان MyLeaveRequests.</span><span class="sxs-lookup"><span data-stu-id="88607-106">The leave request must be saved in the database and must be retrievable through the MyLeaveRequests entity.</span></span>

## <a name="permissions"></a><span data-ttu-id="88607-107">أذونات</span><span class="sxs-lookup"><span data-stu-id="88607-107">Permissions</span></span>

<span data-ttu-id="88607-108">أحد الأذونات التالية مطلوب لاستدعاء واجهة API هذه.</span><span class="sxs-lookup"><span data-stu-id="88607-108">One of the following permissions is required to call this API.</span></span> <span data-ttu-id="88607-109">لمزيد من المعلومات حول الأذونات وكيفية إعدادها، راجع [التخويل](hr-developer-api-authentication.md).</span><span class="sxs-lookup"><span data-stu-id="88607-109">For more information about permissions and how to select them, see [Authentication](hr-developer-api-authentication.md).</span></span>

| <span data-ttu-id="88607-110">نوع الإذن</span><span class="sxs-lookup"><span data-stu-id="88607-110">Permission type</span></span>                    | <span data-ttu-id="88607-111">الأذونات (من الأقل امتيازًا إلى الأكثر امتيازًا)</span><span class="sxs-lookup"><span data-stu-id="88607-111">Permissions (from least privileged to most privileged)</span></span> |
|------------------------------------|--------------------------------------------------------|
| <span data-ttu-id="88607-112">مفوض (حساب عمل أو مدرسة)</span><span class="sxs-lookup"><span data-stu-id="88607-112">Delegated (work or school account)</span></span> | <span data-ttu-id="88607-113">user\_impersonation</span><span class="sxs-lookup"><span data-stu-id="88607-113">user\_impersonation</span></span>                                    |

## <a name="https-request"></a><span data-ttu-id="88607-114">طلب HTTPS</span><span class="sxs-lookup"><span data-stu-id="88607-114">HTTPS request</span></span>

<!-- { "blockType": "ignored" } -->
```HTTP
POST https://{cluster}.hr.talent.dynamics.com/namespaces/{namespace_guid}/data/MyLeaveRequests(RequestId='{requestId}', LeaveType='{leaveType}', LeaveDate={leaveDate}, dataAreaId={dataArea})/Microsoft.Dynamics.DataEntities.submit?cross-company=true
```

<span data-ttu-id="88607-115">يتوافق الطلب مع مقاييس OData.</span><span class="sxs-lookup"><span data-stu-id="88607-115">The request conforms to OData standards.</span></span> <span data-ttu-id="88607-116">تشير المعلمات {requestId} و {leaveType} و {leaveDate}و {dataArea} إلى الحقول التي تشكل المفتاح الطبيعي المركب لكيان MyLeaveRequests.</span><span class="sxs-lookup"><span data-stu-id="88607-116">The {requestId}, {leaveType}, {leaveDate}, and {dataArea} parameters refer to the fields that make up the composite natural key for the MyLeaveRequests entity.</span></span>

> [!NOTE]
> <span data-ttu-id="88607-117">بينما تشير حقول الكيان MyLeaveRequests إلى بند فردي في طلب الإجازه، فان استدعاء واجهة API الخاصة بالإرسال سيرسل طلب الإجازة كاملاً (كافة البنود) إلى سير العمل.</span><span class="sxs-lookup"><span data-stu-id="88607-117">While the fields for the MyLeaveRequests entity refer to an individual line in the leave request, calling the submit API will submit the entire leave request (all lines) to workflow.</span></span>

### <a name="request-headers"></a><span data-ttu-id="88607-118">رؤوس الطلبات</span><span class="sxs-lookup"><span data-stu-id="88607-118">Request headers</span></span>

| <span data-ttu-id="88607-119">رأس</span><span class="sxs-lookup"><span data-stu-id="88607-119">Header</span></span>         | <span data-ttu-id="88607-120">قيمة</span><span class="sxs-lookup"><span data-stu-id="88607-120">Value</span></span>                     |
|----------------|---------------------------|
| <span data-ttu-id="88607-121">التخويل</span><span class="sxs-lookup"><span data-stu-id="88607-121">Authorization</span></span>  | <span data-ttu-id="88607-122">الحامل {token} (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="88607-122">Bearer {token} (required)</span></span> |
| <span data-ttu-id="88607-123">نوع المحتوى</span><span class="sxs-lookup"><span data-stu-id="88607-123">Content-Type</span></span>   | <span data-ttu-id="88607-124">application/json</span><span class="sxs-lookup"><span data-stu-id="88607-124">application/json</span></span>          |

### <a name="request-body"></a><span data-ttu-id="88607-125">نص الطلب</span><span class="sxs-lookup"><span data-stu-id="88607-125">Request body</span></span>

<span data-ttu-id="88607-126">لا تقم بتقديم نص طلب لهذا الأسلوب.</span><span class="sxs-lookup"><span data-stu-id="88607-126">Don't supply a request body for this method.</span></span>

### <a name="response"></a><span data-ttu-id="88607-127">استجابة</span><span class="sxs-lookup"><span data-stu-id="88607-127">Response</span></span>

<span data-ttu-id="88607-128">الاستجابة الناجحة دائمًا هي استجابة **لا يوجود محتوى 204**.</span><span class="sxs-lookup"><span data-stu-id="88607-128">A successful response is always a **204 No Content** response.</span></span>

<span data-ttu-id="88607-129">سيتلقى المتصلون غير المصرح لهم الرد **غير مصرح 401** أو **ممنوع 403**.</span><span class="sxs-lookup"><span data-stu-id="88607-129">Unauthorized callers will receive a **401 Unauthorized** or a **403 Forbidden** response.</span></span>

<span data-ttu-id="88607-130">إذا لم تنجح عملية التسليم (بسبب التحقق من الصحة، على سبيل المثال) ، فان الاستجابة ستكون **خطأ في الخادم 500**، وسيتضمن نص الاستجابة كائن JSON مع مزيد من التفاصيل.</span><span class="sxs-lookup"><span data-stu-id="88607-130">If submission is unsuccessful (because of validation, for example), the response will be a **500 Server Error**, and the response body will include a JSON object with further details.</span></span>

## <a name="example"></a><span data-ttu-id="88607-131">مثال</span><span class="sxs-lookup"><span data-stu-id="88607-131">Example</span></span>

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

## <a name="validation-and-error-messages"></a><span data-ttu-id="88607-132">رسائل التحقق من الصحة ورسائل الخطأ</span><span class="sxs-lookup"><span data-stu-id="88607-132">Validation and error messages</span></span>

<span data-ttu-id="88607-133">كجزء من استدعاء API الخاص بالإرسال، تتحقق الموارد البشرية من صحة منطق العمل قبل الإرسال، مما يضمن وجود طلب الإجازة في حالة صالحة للإرسال.</span><span class="sxs-lookup"><span data-stu-id="88607-133">As part of the call to the submit API, Human Resources performs business logic validation before submission, which ensures the leave request is in a valid state for submission.</span></span> <span data-ttu-id="88607-134">رسائل الخطأ المحتملة التي قد تتلقاها في الاستجابة إذا فشلت عملية التحقق من الصحة:</span><span class="sxs-lookup"><span data-stu-id="88607-134">The possible error messages you may receive in the response if validations fail are:</span></span>

 - <span data-ttu-id="88607-135">قد يضع الطلب الرصيد '{LeaveTypeId}' تحت الحد الأدنى للرصيد المسوح به في {date}.</span><span class="sxs-lookup"><span data-stu-id="88607-135">The request would put the '{LeaveTypeId}' balance below the allowed minimum balance on {date}.</span></span>
 - <span data-ttu-id="88607-136">لا يمكن إرسال طلب زمن التوقف في حالة مكتملة.</span><span class="sxs-lookup"><span data-stu-id="88607-136">Time off request in Completed state cannot be submitted.</span></span>
 - <span data-ttu-id="88607-137">لا يمكن إرسال طلب أو حفظه لأنه لم يتم إجراء أية تغييرات.</span><span class="sxs-lookup"><span data-stu-id="88607-137">Unable to submit or save request as no changes have been made.</span></span> <span data-ttu-id="88607-138">قم بإضافة أو تحديث المبلغ أو نوع الإجازة ثم حاول مرة أخرى.</span><span class="sxs-lookup"><span data-stu-id="88607-138">Add or update the amount or the leave type and try again.</span></span>
 - <span data-ttu-id="88607-139">طلب زمن التوقف الذي أدخلته يحتوي علي يوم واحد أو أكثر بنفس التاريخ ونوع الإجازة كطلب معلق موجود.</span><span class="sxs-lookup"><span data-stu-id="88607-139">The time off request entered contains one or more days with the same date and leave type as an existing pending request.</span></span> <span data-ttu-id="88607-140">الرجاء استدعاء الطلب الموجود لإجراء التغييرات.</span><span class="sxs-lookup"><span data-stu-id="88607-140">Please recall the existing request to make changes.</span></span>
 - <span data-ttu-id="88607-141">لا ينطبق رمز السبب '{ReasonCodeId}' على أي من أنواع الإجازات في الطلب.</span><span class="sxs-lookup"><span data-stu-id="88607-141">Reason code '{ReasonCodeId}' doesn't apply to any of the leave types in the request.</span></span>
 - <span data-ttu-id="88607-142">يتطلب نوع الإجازة '{LeaveTypeId}' رمز سبب.</span><span class="sxs-lookup"><span data-stu-id="88607-142">Leave type '{LeaveTypeId}' requires a reason code.</span></span> <span data-ttu-id="88607-143">حدد النوع المناسب ورمز السبب.</span><span class="sxs-lookup"><span data-stu-id="88607-143">Select the appropriate type and reason code.</span></span>
 - <span data-ttu-id="88607-144">لم يتم إرسال زمن التوقف بنجاح.</span><span class="sxs-lookup"><span data-stu-id="88607-144">The time off was not submitted successfully.</span></span> <span data-ttu-id="88607-145">تم حفظ زمن التوقف كطلب مسودة.</span><span class="sxs-lookup"><span data-stu-id="88607-145">The time off has been saved as a draft request.</span></span>

## <a name="see-also"></a><span data-ttu-id="88607-146">راجع أيضًا</span><span class="sxs-lookup"><span data-stu-id="88607-146">See also</span></span>

- [<span data-ttu-id="88607-147">نظره عامة على MyLeaveRequests</span><span class="sxs-lookup"><span data-stu-id="88607-147">MyLeaveRequests overview</span></span>](hr-developer-api-myleaverequests-overview.md)
- [<span data-ttu-id="88607-148">المصادقة</span><span class="sxs-lookup"><span data-stu-id="88607-148">Authentication</span></span>](hr-developer-api-authentication.md)