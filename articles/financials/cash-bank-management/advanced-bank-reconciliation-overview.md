---
title: "نظرة عامة على التسوية البنكية المتقدمة"
description: "تشرح هذه المقالة تدفق عملية التسويات البنكية المتقدمة. تسمح ميزة التسوية البنكية المتقدمة باستيراد كشوف الحسابات البنكية التي يمكن تسويتها تلقائيًا من داخل الحركات البنكية."
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BankReconciliationMatchRule
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 22104
ms.assetid: b0705653-1fa6-4d94-9728-bcf9fb387ad1
ms.search.region: Global
ms.author: leguo
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 5c6cec76ebc8328f221ecb6c30ae93716bd9bfe9
ms.contentlocale: ar-sa
ms.lasthandoff: 08/07/2018

---

# <a name="advanced-bank-reconciliation-overview"></a><span data-ttu-id="1e167-104">نظرة عامة على التسوية البنكية المتقدمة</span><span class="sxs-lookup"><span data-stu-id="1e167-104">Advanced bank reconciliation overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1e167-105">تشرح هذه المقالة تدفق عملية التسويات البنكية المتقدمة.</span><span class="sxs-lookup"><span data-stu-id="1e167-105">This article describes the flow for the advanced bank reconciliation process.</span></span> <span data-ttu-id="1e167-106">تسمح ميزة التسوية البنكية المتقدمة باستيراد كشوف الحسابات البنكية التي يمكن تسويتها تلقائيًا من داخل الحركات البنكية.</span><span class="sxs-lookup"><span data-stu-id="1e167-106">The advanced bank reconciliation feature lets you import bank statements that can be automatically reconciled from within bank transactions.</span></span>

<span data-ttu-id="1e167-107">تتيح لك ميزة تسوية البنكية المتقدمة استيراد كشوف الحسابات البنكية.</span><span class="sxs-lookup"><span data-stu-id="1e167-107">The advanced bank reconciliation feature lets you import bank statements.</span></span> <span data-ttu-id="1e167-108">ويمكن بعد ذلك تسوية كشف الحساب البنكي المستورد تلقائياً من داخل الحركات البنكية.</span><span class="sxs-lookup"><span data-stu-id="1e167-108">The imported bank statement can then be automatically reconciled from within bank transactions.</span></span> <span data-ttu-id="1e167-109">فيما يلي الخطوات في تدفق التسوية البنكية المتقدمة.</span><span class="sxs-lookup"><span data-stu-id="1e167-109">Here are the steps in the advanced bank reconciliation flow.</span></span>

1.  <span data-ttu-id="1e167-110">إعداد استيراد كشف الحساب البنكي.</span><span class="sxs-lookup"><span data-stu-id="1e167-110">Set up a bank statement import.</span></span>
    -   <span data-ttu-id="1e167-111">استيراد كشوف الحسابات البنكية من خلال إطار كيان البيانات.</span><span class="sxs-lookup"><span data-stu-id="1e167-111">Import bank statements through the data entity framework.</span></span>
    -   <span data-ttu-id="1e167-112">هناك ثلاثة تنسيقات نموذجية لكشف البنك مضمنة في: ISO20022، وBAI2، وMT940.</span><span class="sxs-lookup"><span data-stu-id="1e167-112">Three typical bank statement formats are built in: ISO20022, BAI2, and MT940.</span></span>
    -   <span data-ttu-id="1e167-113">يمكن توسيع الوظائف لأي تنسيق.</span><span class="sxs-lookup"><span data-stu-id="1e167-113">The functionality can be extended to any format.</span></span>

2.  <span data-ttu-id="1e167-114">قم بإعداد تسلسل رقمي لاستخدامه للتسوية البنكية المتقدمة، وحدد قواعد مطابقة التسوية البنكية.</span><span class="sxs-lookup"><span data-stu-id="1e167-114">Set up a number sequence to use for advanced bank reconciliation, and define the bank reconciliation matching rules.</span></span>
    -   <span data-ttu-id="1e167-115">وقاعدة مطابقة التسوية هي مجموعة من المعايير المستخدمة لتصفية بنود كشف الحساب البنكي وبنود الحركات البنكية في Microsoft Dynamics 365 for Finance and Operations أثناء عملية التسوية.</span><span class="sxs-lookup"><span data-stu-id="1e167-115">A reconciliation matching rule is a set of criteria that are used to filter bank statement lines and Microsoft Dynamics 365 for Finance and Operations bank transaction lines during the reconciliation process.</span></span> <span data-ttu-id="1e167-116">واستنادًا إلى ممارسة العمل الخاصة بك، يمكنك إعداد أكثر من قاعدة مطابقة لتحسين عملية التسوية وإجرائها تلقائيًا.‬</span><span class="sxs-lookup"><span data-stu-id="1e167-116">Depending on your business practice, you can set up more than one matching rule to automate and optimize your reconciliation process.</span></span>

3.  <span data-ttu-id="1e167-117">تسوية الكشوف البنكية مع الحركات البنكية في Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="1e167-117">Reconcile bank statements with Finance and Operations bank transactions.</span></span>
    -   <span data-ttu-id="1e167-118">قم بإنشاء دفاتر يومية التسوية ومطابقتها تلقائيًا.</span><span class="sxs-lookup"><span data-stu-id="1e167-118">Perform automatic matching and creation of reconciliation journals.</span></span>
    -   <span data-ttu-id="1e167-119">اعرض الكشوف البنكية والحركات البنكية في Finance and Operations جنبًا إلى جنب.</span><span class="sxs-lookup"><span data-stu-id="1e167-119">View bank statements and Finance and Operations bank transactions side by side.</span></span>
    -   <span data-ttu-id="1e167-120">وقم بترحيل الحركات البنكية في Finance and Operations تلقائياً إذا كانت تظهر في كشف بنكي ولكن لا تظهر في Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="1e167-120">Automatically post Finance and Operations bank transactions if they appear on a bank statement but don't appear in Finance and Operations.</span></span>
    -   <span data-ttu-id="1e167-121">إنشاء كشف تسوية.</span><span class="sxs-lookup"><span data-stu-id="1e167-121">Generate a reconciliation statement.</span></span>






