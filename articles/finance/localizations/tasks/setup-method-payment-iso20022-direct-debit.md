---
title: إعداد طريقة دفع للدين المباشر ISO20022
description: يوضح هذا الإجراء كيفية إعداد طريقة الدفع الخاصة بالعميل للدين المباشر ISO20022 أو أي نوع دفع آخر باستخدام التقارير الإلكترونية.
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPaymMode
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 38afbc3a49d9020540a56e58ce51196b53d6a9e1
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/18/2020
ms.locfileid: "3143422"
---
# <a name="setup-method-of-payment-for-iso20022-direct-debit"></a><span data-ttu-id="cabed-103">إعداد طريقة دفع للدين المباشر ISO20022</span><span class="sxs-lookup"><span data-stu-id="cabed-103">Setup method of payment for ISO20022 direct debit</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="cabed-104">يوضح هذا الإجراء كيفية إعداد طريقة الدفع الخاصة بالعميل للدين المباشر ISO20022 أو أي نوع دفع آخر باستخدام التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="cabed-104">This procedure shows how to set up the customer method of payment for ISO20022 direct debit or any other payment type using electronic reporting.</span></span> 



<span data-ttu-id="cabed-105">قبل إكمال هذه المهمة، يجب إعداد تكوينات تنسيق التصدير وحسابات الدفع.</span><span class="sxs-lookup"><span data-stu-id="cabed-105">Before you complete this task, you must set up export format configurations and payment accounts.</span></span>



<span data-ttu-id="cabed-106">تم إنشاء هذا الإجراء باستخدام شركة بيانات العرض التوضيحي DEMF.</span><span class="sxs-lookup"><span data-stu-id="cabed-106">This procedure was created using the demo data company DEMF.</span></span>



<span data-ttu-id="cabed-107">هذا هو الإجراء الثالث من ضمن خمسة إجراءات هدفها توضيح عملية معالجة مدفوعات العميل باستخدام تكوينات التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="cabed-107">This is the third of five procedures that demonstrate the customer payment process using electronic reporting configurations.</span></span>

1. <span data-ttu-id="cabed-108">انتقل إلى الحسابات المدينة > إعداد الدفعات > طرق الدفع.</span><span class="sxs-lookup"><span data-stu-id="cabed-108">Go to Accounts receivable > Payments setup > Methods of payment.</span></span>
2. <span data-ttu-id="cabed-109">استخدم عامل التصفية السريع للبحث عن السجلات.</span><span class="sxs-lookup"><span data-stu-id="cabed-109">Use the Quick Filter to find records.</span></span> <span data-ttu-id="cabed-110">على سبيل المثال، قم بإجراء التصفية على الحقل "طريقة الدفع" بقيمة "إلكتروني".</span><span class="sxs-lookup"><span data-stu-id="cabed-110">For example, filter on the Method of payment field with a value of 'ELECTRONIC'.</span></span>
3. <span data-ttu-id="cabed-111">انقر فوق "تحرير".</span><span class="sxs-lookup"><span data-stu-id="cabed-111">Click Edit.</span></span>
4. <span data-ttu-id="cabed-112">في الحقل "حساب الدفع"، حدد القيم "DEMF OPER".</span><span class="sxs-lookup"><span data-stu-id="cabed-112">In the Payment account field, specify the values 'DEMF OPER'.</span></span>
5. <span data-ttu-id="cabed-113">وسّع قسم المقطع "تنسيقات الملفات".</span><span class="sxs-lookup"><span data-stu-id="cabed-113">Expand the File formats section.</span></span>
6. <span data-ttu-id="cabed-114">حدد "نعم" في الحقل "التقارير الإلكترونية العامة‬".</span><span class="sxs-lookup"><span data-stu-id="cabed-114">Select Yes in the Generic electronic reporting field.</span></span>
7. <span data-ttu-id="cabed-115">في الحقل "تصدير تكوين التنسيق‬"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="cabed-115">In the Export format configuration field, enter or select a value.</span></span>
    * <span data-ttu-id="cabed-116">في القائمة، حدد قيمة الدين المباشر ISO20022 (DE).</span><span class="sxs-lookup"><span data-stu-id="cabed-116">In the list, select ISO20022 Direct debit (DE).</span></span>  <span data-ttu-id="cabed-117">إذا كانت القائمة فارغة، فهذا يعني أن تكوين تنسيق تصدير دفعات العميل غير مستورد ونشط.</span><span class="sxs-lookup"><span data-stu-id="cabed-117">If the list is empty, the customer payment export format configuration has not been imported and active.</span></span>  
8. <span data-ttu-id="cabed-118">حدد "نعم" في الحقل "مطلوب تفويض‬".</span><span class="sxs-lookup"><span data-stu-id="cabed-118">Select Yes in the Require mandate field.</span></span>
    * <span data-ttu-id="cabed-119">حدد المعلمة "مطلوب تفويض‬" لتنسيقات مدفوعات العميل، التي تتطلب معلومات التفويض‬ في رسالة الدفع، مثل "دين مباشر سيبا‬".</span><span class="sxs-lookup"><span data-stu-id="cabed-119">Select the Require mandate parameter for customer payment formats, which require including mandate information in the payment message, like SEPA direct debit.</span></span>  
9. <span data-ttu-id="cabed-120">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="cabed-120">Click Save.</span></span>
