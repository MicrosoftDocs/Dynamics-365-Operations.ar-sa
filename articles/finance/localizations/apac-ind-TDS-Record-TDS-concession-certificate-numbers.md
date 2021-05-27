---
title: قم بتسجيل أرقام شهادات تخويل TDS
description: يوضح هذا الموضوع كيفية تسجيل أرقام شهادات تخويل الضريبة المخصومة في المصدر (TDS) الصادرة إلى الموردين.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: f543adc8bab5ca224bdb672d6b3c282c2d8531d8
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022986"
---
# <a name="record-tds-concession-certificate-numbers"></a><span data-ttu-id="93585-103">قم بتسجيل أرقام شهادات تخويل TDS</span><span class="sxs-lookup"><span data-stu-id="93585-103">Record TDS concession certificate numbers</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="93585-104">يوضح هذا الموضوع كيفية تسجيل أرقام شهادات تخويل الضريبة المخصومة في المصدر (TDS) الصادرة إلى الموردين.</span><span class="sxs-lookup"><span data-stu-id="93585-104">This topic explains how to record the Tax Deducted at Source (TDS) concession certificate numbers that are issued to vendors.</span></span>

1. <span data-ttu-id="93585-105">انتقل إلى **ضريبة \> ضرائب غير مباشرة \> ضريبة خصم \> تخويلات ضرائب الخصم**.</span><span class="sxs-lookup"><span data-stu-id="93585-105">Go to **Tax \> Indirect taxes \> Withholding tax \> Withholding tax concessions**.</span></span>
2. <span data-ttu-id="93585-106">في الحقل **نوع الضريبة**، حدد **TDS** لتسجيل شهادات التخويل الخاصة بنوع الضريبة TDS.</span><span class="sxs-lookup"><span data-stu-id="93585-106">In the **Tax type** field, select **TDS** to record concession certificates for the TDS tax type.</span></span>
3. <span data-ttu-id="93585-107">في علامة التبويب **نظرة عامة**، حدد **Alt+N** لإنشاء بند.</span><span class="sxs-lookup"><span data-stu-id="93585-107">On the **Overview** tab, select **Alt+N** to create a line.</span></span>

    <span data-ttu-id="93585-108">[![رأس البند الجديد](./media/apac-ind-TDS-34.png)](./media/apac-ind-TDS-34.png)</span><span class="sxs-lookup"><span data-stu-id="93585-108">[![Header of the new line](./media/apac-ind-TDS-34.png)](./media/apac-ind-TDS-34.png)</span></span>

4. <span data-ttu-id="93585-109">في الحقل **كود ضريبة الخصم**، حدد كود الضريبة TDS الذي يتم إصدار شهادات تخويل المورد له.</span><span class="sxs-lookup"><span data-stu-id="93585-109">In the **Withholding tax code** field, select the TDS tax code that the vendor concession certificates are issued for.</span></span> <span data-ttu-id="93585-110">يعرض الحقل **اسم كود ضريبة الخصم** اسم كود ضريبة TDS.</span><span class="sxs-lookup"><span data-stu-id="93585-110">The **Withholding tax code name** field shows the name of the TDS tax code.</span></span>
5. <span data-ttu-id="93585-111">في الحقلين **من تاريخ** و **إلى تاريخ**، حدد فترة الصلاحية لشهادة التخويل التي تستخدم كود الضريبة TDS لحساب TDS للمورد على أساس تيسيري.</span><span class="sxs-lookup"><span data-stu-id="93585-111">In the **From date** and **To date** fields, define the period of validity for the concession certificate that uses the TDS tax code to calculate TDS for the vendor on a concessional basis.</span></span>
6. <span data-ttu-id="93585-112">في الحقل **ملاحظات**، أدخل أية ملاحظات.</span><span class="sxs-lookup"><span data-stu-id="93585-112">In the **Remarks** field, enter any remarks.</span></span>
7. <span data-ttu-id="93585-113">في الحقل **القسم**، أدخل كود القسم القانوني الذي استفادت ضمنه شهادة تخويل TDS.</span><span class="sxs-lookup"><span data-stu-id="93585-113">In the **Section** field, enter the legal section code that the TDS concession certificate is availed under.</span></span>

    <span data-ttu-id="93585-114">إذا كان رمز القسم 197، تظهر القيمة "أ" في كلا العمودين "سبب عدم الخصم/خصم أقل" في النموذج 26Q و"سبب الخصم عدم الخصم/خصم أقل/تضخيم الفائدة (إن وجد)" في النموذج 27Q.</span><span class="sxs-lookup"><span data-stu-id="93585-114">If the section code is 197, the value "A" appears in both the "Reason for non-deduction/lower deduction" column in Form 26Q and the "Reason for non-deduction/lower deduction/grossing up (if any)" column in Form 27Q.</span></span> <span data-ttu-id="93585-115">إذا كان كود القسم 197A، تظهر القيمة "ب" في كلا المكانين.</span><span class="sxs-lookup"><span data-stu-id="93585-115">If the section code is 197A, the value "B" appears in both those places.</span></span>

8. <span data-ttu-id="93585-116">حدد علامة التبويب السريعة **الشهادة** لتسجيل أرقام شهادات تخويل TDS للموردين.</span><span class="sxs-lookup"><span data-stu-id="93585-116">Select the **Certificate** FastTab to record TDS concession certificate numbers for vendors.</span></span>
9. <span data-ttu-id="93585-117">في الحقل **حساب المورد**، حدد حساب المورد الذي يتم إصدار شهادة تخويل TDS له.</span><span class="sxs-lookup"><span data-stu-id="93585-117">In the **Vendor account** field, select the vendor account that the TDS concession certificate is issued for.</span></span>
10. <span data-ttu-id="93585-118">في الحقلين **من تاريخ** و **إلى تاريخ**، حدد فترة الصلاحية لشهادة تخويل TDS.</span><span class="sxs-lookup"><span data-stu-id="93585-118">In the **From date** and **To date** fields, define the period of validity for the TDS concession certificate.</span></span>

    <span data-ttu-id="93585-119">يستند حساب TDS على أساس تيسيري إلى الفترة التي يتم فيها إنشاء الشهادة للمورد.</span><span class="sxs-lookup"><span data-stu-id="93585-119">The calculation of TDS on a concessional basis is based on the period when the certificate is created for the vendor.</span></span>

11. <span data-ttu-id="93585-120">في الحقل **الشهادة**، أدخل رقم شهادة تخويل TDS.</span><span class="sxs-lookup"><span data-stu-id="93585-120">In the **Certificate** field, enter the TDS concession certificate number.</span></span>

    <span data-ttu-id="93585-121">[![علامة التبويب السريعة الشهادة](./media/apac-ind-TDS-33.png)](./media/apac-ind-TDS-33.png)</span><span class="sxs-lookup"><span data-stu-id="93585-121">[![Certificate FastTab](./media/apac-ind-TDS-33.png)](./media/apac-ind-TDS-33.png)</span></span>

12. <span data-ttu-id="93585-122">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="93585-122">Close the page.</span></span>
