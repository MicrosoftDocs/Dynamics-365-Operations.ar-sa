---
title: إعداد هيئات ضريبة الخصم لنوع ضريبة TDS
description: يوضح هذا الموضوع كيفية إعداد هيئة الضريبة المخصومة في المصدر (TDS).
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
ms.openlocfilehash: 5375363a9b1383a83e80fc3c4b841780adab4172
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022990"
---
# <a name="set-up-withholding-tax-authorities-for-the-tds-tax-type"></a><span data-ttu-id="b4868-103">إعداد هيئات ضريبة الخصم لنوع ضريبة TDS</span><span class="sxs-lookup"><span data-stu-id="b4868-103">Set up withholding tax authorities for the TDS tax type</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b4868-104">يوضح هذا الموضوع كيفية إعداد هيئة الضريبة المخصومة في المصدر (TDS).</span><span class="sxs-lookup"><span data-stu-id="b4868-104">This topic explains how to set up Tax Deducted at Source (TDS) authorities.</span></span>

1. <span data-ttu-id="b4868-105">انتقل إلى **الضريبة \> ضرائب غير مباشرة \> هيئات ضريبة الخصم**.</span><span class="sxs-lookup"><span data-stu-id="b4868-105">Go to **Tax \> Indirect taxes \> Withholding tax authorities**.</span></span>

    <span data-ttu-id="b4868-106">[![صفحة هيئات ضريبة الخصم](./media/apac-ind-TDS-12.png)](./media/apac-ind-TDS-12.png)</span><span class="sxs-lookup"><span data-stu-id="b4868-106">[![Withholding tax authorities page](./media/apac-ind-TDS-12.png)](./media/apac-ind-TDS-12.png)</span></span>

2. <span data-ttu-id="b4868-107">في الحقل **نوع الضريبة**، حدد **TDS** لإعداد هيئات ضريبة الخصم لنوع الضريبة TDS.</span><span class="sxs-lookup"><span data-stu-id="b4868-107">In the **Tax type** field, select **TDS** to set up withholding tax authorities for the TDS tax type.</span></span>
3. <span data-ttu-id="b4868-108">في جزء الإجراءات، حدد **جديد** لإنشاء بند.</span><span class="sxs-lookup"><span data-stu-id="b4868-108">On the Action Pane, select **New** to create a line.</span></span>
4. <span data-ttu-id="b4868-109">في الحقل **هيئة ضريبة الخصم**، أدخل اسمًا لهيئة TDS.</span><span class="sxs-lookup"><span data-stu-id="b4868-109">In the **Withholding tax authority** field, enter a name for the TDS authority.</span></span>
5. <span data-ttu-id="b4868-110">في الحقل **الوصف**، أدخل وصفًا.</span><span class="sxs-lookup"><span data-stu-id="b4868-110">In the **Description** field, enter a description.</span></span>
6. <span data-ttu-id="b4868-111">في علامة التبويب السريعة **عام**، في الحقل **حساب المورد**، حدد حساب المورد لهيئة TDS.</span><span class="sxs-lookup"><span data-stu-id="b4868-111">On the **General** FastTab, in the **Vendor account** field, select the vendor account for the TDS authority.</span></span>

    > [!NOTE]
    > <span data-ttu-id="b4868-112">يجب تحديد اسم البنك حيث سيتم إيداع الأموال المستحقة لمورد هيئة TDS.</span><span class="sxs-lookup"><span data-stu-id="b4868-112">You must define the name of the bank where funds that are owed to the TDS authority vendor will be deposited.</span></span> <span data-ttu-id="b4868-113">يتم تحديد اسم البنك في الصفحة **حسابات البنك** (**الحسابات الدائنة \> جميع الموردين \> المورد \> إعداد \> حسابات البنك**).</span><span class="sxs-lookup"><span data-stu-id="b4868-113">The bank's name is defined on the **Bank accounts** page (**Accounts payable \> All vendors \> Vendor \> Set up \> Bank accounts**).</span></span>

7. <span data-ttu-id="b4868-114">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="b4868-114">Close the page.</span></span>
