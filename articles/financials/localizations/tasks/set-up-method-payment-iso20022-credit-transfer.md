--- 
title: "إعداد طريقة دفع لتحويل الائتمان ISO20022"
description: "يوضح هذا الإجراء كيفية إعداد طريقة الدفع الخاصة بالمورّد لتحويل الائتمان ISO20022 أو أي نوع دفع آخر باستخدام التقارير الإلكترونية لإنشاء ملف."
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: VendPaymMode
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: c9209006074fb9da2c3c2ffaa2af4adecfcc1aa9
ms.contentlocale: ar-sa
ms.lasthandoff: 09/14/2018

---
# <a name="set-up-method-of-payment-for-iso20022-credit-transfer"></a><span data-ttu-id="13ee2-103">إعداد طريقة دفع لتحويل الائتمان ISO20022</span><span class="sxs-lookup"><span data-stu-id="13ee2-103">Set up method of payment for ISO20022 credit transfer</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="13ee2-104">يوضح هذا الإجراء كيفية إعداد طريقة الدفع الخاصة بالمورّد لتحويل الائتمان ISO20022 أو أي نوع دفع آخر باستخدام التقارير الإلكترونية لإنشاء ملف.</span><span class="sxs-lookup"><span data-stu-id="13ee2-104">This procedure shows how to set up the vendor method of payment for ISO20022 credit transfer or any other payment type using electronic reporting to generate a file.</span></span> 

<span data-ttu-id="13ee2-105">قبل إكمال هذه المهمة، يجب تصدير تكوينات التنسيق وإعداد حسابات الدفع.</span><span class="sxs-lookup"><span data-stu-id="13ee2-105">Before you complete this task, you must export format configurations and set up payment accounts.</span></span>

<span data-ttu-id="13ee2-106">تم إنشاء هذه المهمة باستخدام شركة بيانات العرض التوضيحي DEMF.</span><span class="sxs-lookup"><span data-stu-id="13ee2-106">This task was created using the DEMF demo data company.</span></span>

<span data-ttu-id="13ee2-107">هذا هو الإجراء الثالث من ضمن الإجراءات الخمسة، هدفه توضيح عملية معالجة مدفوعات المورّد باستخدام تكوينات التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="13ee2-107">This is the third procedure, out of five, that illustrates the vendor payment process using electronic reporting configurations.</span></span> <span data-ttu-id="13ee2-108">يتم استخدام هذا الإجراء لميزة تمت إضافتها في Dynamics 365 for Operations، الإصدار 1611.</span><span class="sxs-lookup"><span data-stu-id="13ee2-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>

1. <span data-ttu-id="13ee2-109">انتقل إلى الحسابات المدينة > إعداد الدفع‬ > طرق الدفع.</span><span class="sxs-lookup"><span data-stu-id="13ee2-109">Go to Accounts payable > Payment setup > Methods of payment.</span></span>
2. <span data-ttu-id="13ee2-110">استخدم عامل التصفية السريع للبحث عن السجلات.</span><span class="sxs-lookup"><span data-stu-id="13ee2-110">Use the Quick Filter to find records.</span></span> <span data-ttu-id="13ee2-111">على سبيل المثال، قم بإجراء التصفية على الحقل "طريقة الدفع" بقيمة "سيبا CT".</span><span class="sxs-lookup"><span data-stu-id="13ee2-111">For example, filter on the Method of payment field with a value of 'SEPA CT'.</span></span>
3. <span data-ttu-id="13ee2-112">انقر فوق "تحرير".</span><span class="sxs-lookup"><span data-stu-id="13ee2-112">Click Edit.</span></span>
4. <span data-ttu-id="13ee2-113">الحقل "الفترة"، حدد "الإجمالي".</span><span class="sxs-lookup"><span data-stu-id="13ee2-113">In the Period field, select 'Total'.</span></span>
5. <span data-ttu-id="13ee2-114">في الحقل "نوع الدفع"، حدد "دفع إلكتروني".</span><span class="sxs-lookup"><span data-stu-id="13ee2-114">In the Payment type field, select 'Electronic payment'.</span></span>
6. <span data-ttu-id="13ee2-115">وسّع قسم المقطع "تنسيقات الملفات".</span><span class="sxs-lookup"><span data-stu-id="13ee2-115">Expand the File formats section.</span></span>
7. <span data-ttu-id="13ee2-116">حدد "نعم" في الحقل "التقارير الإلكترونية العامة‬".</span><span class="sxs-lookup"><span data-stu-id="13ee2-116">Select Yes in the Generic electronic reporting field.</span></span>
8. <span data-ttu-id="13ee2-117">في الحقل "تصدير تكوين التنسيق‬"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="13ee2-117">In the Export format configuration field, enter or select a value.</span></span>
    * <span data-ttu-id="13ee2-118">في القائمة، حدد قيمة تحويل الرصيد ISO20022 (DE).</span><span class="sxs-lookup"><span data-stu-id="13ee2-118">In the list, select the value ISO20022 Credit transfer (DE).</span></span> <span data-ttu-id="13ee2-119">إذا كانت القائمة فارغة، فهذا يعني أن تكوين تنسيق تصدير دفعات المورّد غير مستورد ونشط.</span><span class="sxs-lookup"><span data-stu-id="13ee2-119">If the list is empty, the vendor payment export format configuration is not imported and active.</span></span>  
9. <span data-ttu-id="13ee2-120">في الحقل "نوع الحساب"، اكتب "البنك‬".</span><span class="sxs-lookup"><span data-stu-id="13ee2-120">In the Account type field, select 'Bank'.</span></span>
10. <span data-ttu-id="13ee2-121">في الحقل "حساب الدفع"، حدد القيم "DEMF OPER".</span><span class="sxs-lookup"><span data-stu-id="13ee2-121">In the Payment account field, specify the values 'DEMF OPER'.</span></span>
11. <span data-ttu-id="13ee2-122">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="13ee2-122">Click Save.</span></span>


