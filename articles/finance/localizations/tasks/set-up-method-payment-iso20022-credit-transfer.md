---
title: إعداد طريقة دفع لتحويل الائتمان ISO20022
description: يوضح هذا الإجراء كيفية إعداد طريقة الدفع الخاصة بالمورّد لتحويل الائتمان ISO20022 أو أي نوع دفع آخر باستخدام التقارير الإلكترونية لإنشاء ملف.
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendPaymMode
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d6d60502cd7f749b71cf39cc38d8a39dcbb7b108
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/13/2020
ms.locfileid: "4439794"
---
# <a name="set-up-method-of-payment-for-iso20022-credit-transfer"></a><span data-ttu-id="f5586-103">إعداد طريقة دفع لتحويل الائتمان ISO20022</span><span class="sxs-lookup"><span data-stu-id="f5586-103">Set up method of payment for ISO20022 credit transfer</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f5586-104">يوضح هذا الإجراء كيفية إعداد طريقة الدفع الخاصة بالمورّد لتحويل الائتمان ISO20022 أو أي نوع دفع آخر باستخدام التقارير الإلكترونية لإنشاء ملف.</span><span class="sxs-lookup"><span data-stu-id="f5586-104">This procedure shows how to set up the vendor method of payment for ISO20022 credit transfer or any other payment type using electronic reporting to generate a file.</span></span> 

<span data-ttu-id="f5586-105">قبل إكمال هذه المهمة، يجب تصدير تكوينات التنسيق وإعداد حسابات الدفع.</span><span class="sxs-lookup"><span data-stu-id="f5586-105">Before you complete this task, you must export format configurations and set up payment accounts.</span></span>

<span data-ttu-id="f5586-106">تم إنشاء هذه المهمة باستخدام شركة بيانات العرض التوضيحي DEMF.</span><span class="sxs-lookup"><span data-stu-id="f5586-106">This task was created using the DEMF demo data company.</span></span>

<span data-ttu-id="f5586-107">هذا هو الإجراء الثالث من ضمن الإجراءات الخمسة، هدفه توضيح عملية معالجة مدفوعات المورّد باستخدام تكوينات التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="f5586-107">This is the third procedure, out of five, that illustrates the vendor payment process using electronic reporting configurations.</span></span> <span data-ttu-id="f5586-108">يتم استخدام هذا الإجراء لميزة تمت إضافتها في Dynamics 365 for Operations، الإصدار 1611.</span><span class="sxs-lookup"><span data-stu-id="f5586-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>

1. <span data-ttu-id="f5586-109">انتقل إلى الحسابات المدينة > إعداد الدفع‬ > طرق الدفع.</span><span class="sxs-lookup"><span data-stu-id="f5586-109">Go to Accounts payable > Payment setup > Methods of payment.</span></span>
2. <span data-ttu-id="f5586-110">استخدم عامل التصفية السريع للبحث عن السجلات.</span><span class="sxs-lookup"><span data-stu-id="f5586-110">Use the Quick Filter to find records.</span></span> <span data-ttu-id="f5586-111">على سبيل المثال، قم بإجراء التصفية على الحقل "طريقة الدفع" بقيمة "سيبا CT".</span><span class="sxs-lookup"><span data-stu-id="f5586-111">For example, filter on the Method of payment field with a value of 'SEPA CT'.</span></span>
3. <span data-ttu-id="f5586-112">انقر فوق "تحرير".</span><span class="sxs-lookup"><span data-stu-id="f5586-112">Click Edit.</span></span>
4. <span data-ttu-id="f5586-113">الحقل "الفترة"، حدد "الإجمالي".</span><span class="sxs-lookup"><span data-stu-id="f5586-113">In the Period field, select 'Total'.</span></span>
5. <span data-ttu-id="f5586-114">في الحقل "نوع الدفع"، حدد "دفع إلكتروني".</span><span class="sxs-lookup"><span data-stu-id="f5586-114">In the Payment type field, select 'Electronic payment'.</span></span>
6. <span data-ttu-id="f5586-115">وسّع قسم المقطع "تنسيقات الملفات".</span><span class="sxs-lookup"><span data-stu-id="f5586-115">Expand the File formats section.</span></span>
7. <span data-ttu-id="f5586-116">حدد "نعم" في الحقل "التقارير الإلكترونية العامة‬".</span><span class="sxs-lookup"><span data-stu-id="f5586-116">Select Yes in the Generic electronic reporting field.</span></span>
8. <span data-ttu-id="f5586-117">في الحقل "تصدير تكوين التنسيق‬"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="f5586-117">In the Export format configuration field, enter or select a value.</span></span>
    * <span data-ttu-id="f5586-118">في القائمة، حدد قيمة تحويل الرصيد ISO20022 (DE).</span><span class="sxs-lookup"><span data-stu-id="f5586-118">In the list, select the value ISO20022 Credit transfer (DE).</span></span> <span data-ttu-id="f5586-119">إذا كانت القائمة فارغة، فهذا يعني أن تكوين تنسيق تصدير دفعات المورّد غير مستورد ونشط.</span><span class="sxs-lookup"><span data-stu-id="f5586-119">If the list is empty, the vendor payment export format configuration is not imported and active.</span></span>  
9. <span data-ttu-id="f5586-120">في الحقل "نوع الحساب"، اكتب "البنك‬".</span><span class="sxs-lookup"><span data-stu-id="f5586-120">In the Account type field, select 'Bank'.</span></span>
10. <span data-ttu-id="f5586-121">في الحقل "حساب الدفع"، حدد القيم "DEMF OPER".</span><span class="sxs-lookup"><span data-stu-id="f5586-121">In the Payment account field, specify the values 'DEMF OPER'.</span></span>
11. <span data-ttu-id="f5586-122">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="f5586-122">Click Save.</span></span>

